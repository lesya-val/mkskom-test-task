<template>
  <div class="user-profile">
		<div class="user-profile__content">
			<ProfileCard
				:profileSrc="profile"
			/>
			<BlockMenu/>
		</div>
		<SocialMedia/>
  </div>
</template>

<script>

import ProfileCard from '@/components/ProfileCard.vue'
import BlockMenu from '@/components/BlockMenu.vue'
import SocialMedia from '@/components/SocialMedia.vue'

export default {
  name: 'UserPage',
  components: {
    ProfileCard,
		BlockMenu,
		SocialMedia,
  },
	data() {
		return {
			profile: require('../assets/image/profile.png'),
		}
	}
}
</script>