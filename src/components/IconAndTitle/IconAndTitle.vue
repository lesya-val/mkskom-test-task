<template>
  <div :class="$style['icon-and-title']">
    <div :class="$style['icon-and-title__title']">
      <span v-html="icon"></span>
      <h3>{{ title }}</h3>
    </div>
    <p>{{ number }}</p>
  </div>
</template>

<script>

import styles from '@/components/IconAndTitle/IconAndTitle.module.scss'

export default {
  name: "IconAndTitle",
	props: {
		icon: {
			type: String,
			required: true,
		},
		title: {
			type: String,
			required: true,
		},
		number: {
			type: Number,
			required: false,
		},
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>