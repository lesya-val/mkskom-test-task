<template>
  <div :class="$style['main-page']">
		<NavigationBar @searchAlbum="handleSearchAlbum" />
    <div :class="$style['main-page__content']">
      <SidePanel />
      <UserProfile />
      <div :class="$style['gallery-editor']">
				<SidebarGallery/>
				<PartGallery :albumId="currentAlbumId" />
			</div>
    </div>
  </div>
</template>

<script>

import NavigationBar from '@/components/NavigationBar/NavigationBar.vue'
import SidePanel from '@/components/SidePanel/SidePanel.vue'
import UserProfile from '@/components/UserProfile/UserProfile.vue'
import SidebarGallery from '@/components/SidebarGallery/SidebarGallery.vue'
import PartGallery from '@/components/PartGallery/PartGallery.vue'
import styles from '@/pages/MainPage/MainPage.module.scss'

export default {
  name: 'MainPage',
  components: {
    NavigationBar,
		SidePanel,
		UserProfile,
		SidebarGallery,
		PartGallery,
  },
	data() {
		return {
			currentAlbumId: null
		}
	},
	methods: {
		handleSearchAlbum(albumId) {
			this.currentAlbumId = albumId;
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>