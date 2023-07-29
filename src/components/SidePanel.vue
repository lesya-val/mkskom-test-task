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

import IconButton from '@/components/UI/IconButton.vue';
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

from '@/assets/js/icons.js'

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

			avatar1: require('../assets/image/avatars/avatar1.png'),
			avatar2: require('../assets/image/avatars/avatar2.png'),
			avatar3: require('../assets/image/avatars/avatar3.png'),
			avatar4: require('../assets/image/avatars/avatar4.png'),
		}
	}
}
</script>