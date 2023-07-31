<template>
  <button :class="$style['icon-button']" type="button">
    <span v-html="icon" :class="$style['icon']"></span>
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
  },
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>