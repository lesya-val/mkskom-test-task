<template>
  <div :class="$style['part-gallery']">
    <EditGallery/>
    <div :class="$style['part-gallery__list']">
      <GalleryItem/>
    </div>
  </div>
</template>

<script>

import EditGallery from '@/components/EditGallery/EditGallery.vue'
import styles from '@/components/PartGallery/PartGallery.module.scss'

export default {
  name: "PartGallery",
  components: {
		EditGallery
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>