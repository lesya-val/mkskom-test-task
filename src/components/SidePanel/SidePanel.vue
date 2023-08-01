<template>
  <aside :class="$style['side-panel']">
    <div :class="$style['side-panel__btns']">
      <IconButton v-for="(button, index) in buttons" :key="index" :icon="button.icon" 
				:isActive="index === activeIcon"
        @click="handleIconButton(index)"
			/>
    </div>
    <div :class="$style['side-panel__avatars']">
      <AvatarItem v-for="(avatar, index) in avatars" :key="index" :src="avatar.src" />
      <IconButton :icon="plus" />
    </div>
  </aside>
</template>

<script>

import IconButton from '@/components/UI/IconButton/IconButton.vue';
import AvatarItem from '@/components/AvatarItem/AvatarItem.vue'
import { compass, star, message, statistics, planet, house, plus, } from '@/assets/js/icons.js'
import { avatar1, avatar2, avatar3, avatar4, } from '@/assets/js/avatars.js'
import styles from '@/components/SidePanel/SidePanel.module.scss'

export default {
  name: 'SidePanel',
  components: {
    IconButton,
		AvatarItem,
  },
	data() {
		return {
			compass: compass,
			star: star,
			message: message,
			statistics: statistics,
			planet: planet,
			house: house,
			plus: plus,

			avatar1: avatar1,
			avatar2: avatar2,
			avatar3: avatar3,
			avatar4: avatar4,

			buttons: [
      { icon: compass },
      { icon: star },
      { icon: message },
      { icon: statistics },
      { icon: planet },
      { icon: house },
			],
			avatars: [
				{ src: avatar1 },
				{ src: avatar2 },
				{ src: avatar3 },
				{ src: avatar4 },
			],
			activeIcon: null,
		}
	},
	methods: {
		handleIconButton(index) {
			this.activeIcon = index;
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>