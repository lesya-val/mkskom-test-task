<template>
  <div class="profile-card">
    <div class="profile-card__btns">
			<IconButton
				:iconButton="user"
			/>
			<IconButton
				:iconButton="ellipsis"
			/>
		</div>
		<div class="profile-card__info">
			<div class="profile-card__img">
				<img :src="profileSrc" alt="Profile">
			</div>
			<div class="profile-card__user">
				<h2 class="profile-card__name">Hello {{ name }}</h2>
				<p class="profile-card__mail">{{ mail }}</p>
			</div>
		</div>
  </div>
</template>

<script>

import IconButton from '@/components/IconButton.vue';

import { 
	user,
	ellipsis,
} 
from '@/assets/js/icons';

export default {
  name: 'ProfileCard',
  components: {
    IconButton
	},
	data() {
		return {
			user: user,
			ellipsis: ellipsis,
			name:'Alfred Bryant',
			mail: 'adrain.nader@yahoo.com',
		}
	},
	props: {
		profileSrc: {
      type: String,
      required: true,
    },
	}
}
</script>