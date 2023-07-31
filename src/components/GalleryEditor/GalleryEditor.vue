<template>
  <div :class="$style['gallery-editor']">
    <SidebarGallery/>
    <GalleryList/>
  </div>
</template>

<script>

import SidebarGallery from '@/components/SidebarGallery/SidebarGallery.vue'

import styles from '@/components/GalleryEditor/GalleryEditor.module.scss'

export default {
  name: "GalleryEditor",
  components: {
		SidebarGallery,
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>