<template>
  <div :class="$style['icon-social']">
    <span v-html="icon" :class="$style['icon']"></span>
  </div>
</template>

<script>

import styles from '@/components/IconSocial/IconSocial.module.scss'

export default {
  name: 'SocialMedia',
	props: {
		icon: {
			type: String,
			required: true,
		},
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>