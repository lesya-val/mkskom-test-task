<template>
  <div :class="$style['gallery-editor']">
    <SidebarGallery/>
    <PartGallery/>
  </div>
</template>

<script>

import SidebarGallery from '@/components/SidebarGallery/SidebarGallery.vue'
import PartGallery from '@/components/PartGallery/PartGallery.vue'
import styles from '@/components/GalleryEditor/GalleryEditor.module.scss'

export default {
  name: "GalleryEditor",
  components: {
		SidebarGallery,
		PartGallery,
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>