<template>
  <div :class="getRowClass">
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
import styles from '@/components/GridRow/GridRow.module.scss';

export default {
	name: 'GridRow',
  components: {
    PhotoCard,
  },
  props: {
    photos: Array,
    columns: Number,
  },
  computed: {
    $style() {
      return styles;
    },
    getRowClass() {
      return this.$style['grid-row-' + this.columns];
    },
  },
};
</script>