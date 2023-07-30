<template>
  <div class="gallery-editor">
		<SidebarGallery/>
		<GalleryList/>
	</div>

</template>

<script>

import SidebarGallery from '@/components/SidebarGallery.vue'

export default {
  name: "GalleryEditor",
  components: {
		SidebarGallery,
	}
};

</script>