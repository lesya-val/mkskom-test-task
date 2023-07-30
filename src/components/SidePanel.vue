<template>
  <aside class="side-panel">
		<div class="side-panel__btns">
			<IconButton
				:iconButton="compass"
			/>
			<IconButton
				:iconButton="star"
			/>
			<IconButton
				:iconButton="message"
			/>
			<IconButton
				:iconButton="statistics"
			/>
			<IconButton
				:iconButton="planet"
			/>
			<IconButton
				:iconButton="house"
			/>
		</div>
		<div class="side-panel__avatars">
			<AvatarItem
				:avatarSrc="avatar1"
			/>
			<AvatarItem
				:avatarSrc="avatar2"
			/>
			<AvatarItem
				:avatarSrc="avatar3"
			/>
			<AvatarItem
				:avatarSrc="avatar4"
			/>
			<IconButton
			:iconButton="plus"
		/>
		</div>
	</aside>
</template>

<script>

import IconButton from '@/components/IconButton.vue';
import AvatarItem from '@/components/AvatarItem.vue'

import { 
	compass,
	star,
	message,
	statistics,
	planet,
	house,
	plus,
} 
from '@/assets/js/iconsButton.js'

import {
	avatar1,
	avatar2,
	avatar3,
	avatar4,
}
from '@/assets/js/avatarsImage'

export default {
  name: 'ContentPart',
  components: {
    IconButton,
		AvatarItem,
  },
	data() {
		return {
			compass: compass,
			star: star,
			message: message,
			statistics: statistics,
			planet: planet,
			house: house,
			plus: plus,

			avatar1: avatar1,
			avatar2: avatar2,
			avatar3: avatar3,
			avatar4: avatar4,
		}
	}
}
</script>