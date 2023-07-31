<template>
  <div :class="$style['grid-row-three']">
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
import styles from '@/components/GridRowThree/GridRowThree.module.scss';

export default {
	name: 'GridRowThree',
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