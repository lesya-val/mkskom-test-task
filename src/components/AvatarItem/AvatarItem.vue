<template>
  <button :class="$style.avatar">
    <img :src="src" alt="Avatar">
  </button>
</template>

<script>

import styles from '@/components/AvatarItem/AvatarItem.module.scss';

export default {
  name: 'AvatarItem',
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