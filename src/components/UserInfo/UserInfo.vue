<template>
	<div :class="$style['user']">
    <div :class="$style['user__img']">
      <span v-html="icon"></span>
    </div>
    <h2 :class="$style['user__name']">{{ name }}</h2>
  </div>
</template>

<script>

import styles from '@/components/UserInfo/UserInfo.module.scss'

export default {
	name: "NavigationUser",
	props: {
    icon: {
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