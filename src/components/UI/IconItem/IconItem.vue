<template>
    <span v-html="icon"></span>
</template>

<script>

import styles from '@/components/UI/IconItem/IconItem.module.scss'

export default {
  name: "IconItem",
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