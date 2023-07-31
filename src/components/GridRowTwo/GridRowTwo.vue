<template>
  <div :class="$style['grid-row-two']">
    <PhotoCard
      :class="$style['grid-item']"
      v-for="photo in photos"
      :key="photo.id"
      :src="photo.url"
    />
  </div>
</template>

<script>
import PhotoCard from '@/components/PhotoCard/PhotoCard.vue';
import styles from '@/components/GridRowTwo/GridRowTwo.module.scss';

export default {
	name: 'GridRowTwo',
  components: {
    PhotoCard,
  },
  props: {
    photos: Array,
  },
  computed: {
    $style() {
      return styles;
    },
  },
};
</script>