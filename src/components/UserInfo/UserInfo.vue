<template>
	<div :class="$style['user']">
    <div :class="$style['user__img']">
      <IconItem :icon="user"/>
    </div>
    <h2 :class="$style['user__name']">{{ name }}</h2>
  </div>
</template>

<script>

import IconItem from '@/components/UI/IconItem/IconItem.vue'
import { user } from '@/assets/js/icons.js'
import styles from '@/components/UserInfo/UserInfo.module.scss'

export default {
	name: "NavigationUser",
	components: {
		IconItem,
	},
	props: {
		name: {
			type: String,
      required: true,
		}
  },
	data() {
		return {
			user: user,
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>