<template>
  <div :class="$style['menu-item']">
    <div :class="$style['menu-item__icon']">
      <span v-html="icon"></span>
    </div>
    <h3 :class="$style['menu-item__title']">{{ title }}</h3>
  </div>
</template>

<script>

import styles from '@/components/MenuItem/MenuItem.module.scss'

export default {
  name: 'MenuItem',
	props: {
		icon: {
      type: String,
      required: true,
    },
		title: {
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