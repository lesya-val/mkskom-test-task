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

import {
	profile
}
from '@/assets/js/avatarsImage'

export default {
  name: 'UserPage',
  components: {
    ProfileCard,
		BlockMenu,
		SocialMedia,
  },
	data() {
		return {
			profile: profile,
		}
	}
}
</script>