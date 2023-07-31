<template>
  <div :class="$style['main-page']">
    <NavigationBar />
    <div :class="$style['main-page__content']">
      <SidePanel />
      <UserProfile />
      <GalleryEditor />
    </div>
  </div>
</template>

<script>

import NavigationBar from '@/components/NavigationBar/NavigationBar.vue'
import SidePanel from '@/components/SidePanel/SidePanel.vue'
import UserProfile from '@/components/UserProfile/UserProfile.vue'
import GalleryEditor from '@/components/GalleryEditor/GalleryEditor.vue'

import styles from '@/pages/MainPage/MainPage.module.scss'

export default {
  name: 'MainPage',
  components: {
    NavigationBar,
		SidePanel,
		UserProfile,
		GalleryEditor,
  },
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>