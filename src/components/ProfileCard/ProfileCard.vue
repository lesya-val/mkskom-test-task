<template>
   <div :class="$style['profile-card']">
    <div :class="$style['profile-card__btns']">
      <IconButton :icon="user" />
      <IconButton :icon="ellipsis" />
    </div>
    <div :class="$style['profile-card__info']">
      <div :class="$style['profile-card__img']">
        <img :src="src" alt="Profile">
      </div>
      <div :class="$style['profile-card__user']">
        <h2 :class="$style['profile-card__name']">Hello {{ name }}</h2>
        <p :class="$style['profile-card__mail']">{{ mail }}</p>
      </div>
    </div>
  </div>
</template>

<script>

import IconButton from '@/components/UI/IconButton/IconButton.vue';
import { user, ellipsis, } from '@/assets/js/icons.js';
import styles from '@/components/ProfileCard/ProfileCard.module.scss'

export default {
  name: 'ProfileCard',
  components: {
    IconButton
	},
	data() {
		return {
			user: user,
			ellipsis: ellipsis,
			name:'Alfred Bryant',
			mail: 'adrain.nader@yahoo.com',
		}
	},
	props: {
		src: {
      type: String,
      required: true,
    },
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>