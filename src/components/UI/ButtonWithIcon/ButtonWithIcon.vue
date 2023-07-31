<template>
  <button :class="$style['button-with-icon']">
    <span v-html="icon"></span>
    <button :class="$style['button-with-icon__btn']">{{ name }}</button>
  </button>
</template>

<script>

import styles from '@/components/UI/ButtonWithIcon/ButtonWithIcon.module.scss'

export default {
  name: "ButtonWithIcon",
	props: {
		icon:  {
			type: String,
      required: true,
		},
		name: {
			type: String,
      required: true,
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>