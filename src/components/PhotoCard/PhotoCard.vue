<template>
  <div :class="$style['photo-card']">
    <div :class="$style['photo-card__img']">
      <img :src="src" alt="Photo">
    </div>
    <div :class="$style['photo-card__info']">
      <h3 :class="$style['photo-card__title']">{{ title }}</h3>
      <p :class="$style['photo-card__data']">{{ data }}</p>
    </div>
  </div>
</template>

<script>

import styles from '@/components/PhotoCard/PhotoCard.module.scss'

export default {
  name: "PhotoCard",
	props: {
		src: {
			type : String,
			require: true,
		},
		title: {
			type : String,
			require: true,
		},
		data: {
			type : String,
			require: true,
		},
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>