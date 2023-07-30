<template>
  <div class="main-page">
    <NavigationBar/>
		<div class="main-page__content">
			<SidePanel/>
			<UserProfile/>
			<GalleryEditor/>
		</div>
  </div>
</template>

<script>

import NavigationBar from '@/components/NavigationBar.vue'
import SidePanel from '@/components/SidePanel.vue'
import UserProfile from '@/components/UserProfile.vue'


export default {
  name: 'MainPage',
  components: {
    NavigationBar,
		SidePanel,
		UserProfile,
  }
}
</script>