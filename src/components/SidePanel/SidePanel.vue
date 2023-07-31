<template>
  <aside :class="$style['side-panel']">
    <div :class="$style['side-panel__btns']">
      <IconButton :icon="compass" />
      <IconButton :icon="star" />
      <IconButton :icon="message" />
      <IconButton :icon="statistics" />
      <IconButton :icon="planet" />
      <IconButton :icon="house" />
    </div>
    <div :class="$style['side-panel__avatars']">
      <AvatarItem :src="avatar1" />
      <AvatarItem :src="avatar2" />
      <AvatarItem :src="avatar3" />
      <AvatarItem :src="avatar4" />
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
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>