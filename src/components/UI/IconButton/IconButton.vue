<template>
  <button 
		:class="[$style['icon-button'], {[$style['icon-button--active']]: isActive}]" 
		@click="handleClick" 
		type="button">
    <span v-html="icon"></span>
  </button>
</template>

<script>

import styles from '@/components/UI/IconButton/IconButton.module.scss'

export default {
  name: "IconButton",
  props: {
    icon: {
      type: String,
      required: true,
    },
		isActive: {
			type: Boolean,
			required: true,
		}
  },
	methods: {
		handleClick() {
			this.$emit('click')
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
};
</script>