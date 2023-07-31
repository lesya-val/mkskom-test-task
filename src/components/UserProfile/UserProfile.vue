<template>
  <div :class="$style['user-profile']">
		<div :class="$style['user-profile__content']">
			<ProfileCard :src="profile" />
			<BlockMenu />
		</div>
		<SocialMedia />
	</div>
</template>

<script>

import ProfileCard from '@/components/ProfileCard/ProfileCard.vue'
import BlockMenu from '@/components/BlockMenu/BlockMenu.vue'
import SocialMedia from '@/components/SocialMedia/SocialMedia.vue'
import { profile } from '@/assets/js/avatars.js'
import styles from '@/components/UserProfile/UserProfile.module.scss'

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
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>