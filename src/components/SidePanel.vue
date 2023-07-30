<template>
  <aside class="side-panel">
		<div class="side-panel__btns">
			<IconButton
				:icon="compass"
			/>
			<IconButton
				:icon="star"
			/>
			<IconButton
				:icon="message"
			/>
			<IconButton
				:icon="statistics"
			/>
			<IconButton
				:icon="planet"
			/>
			<IconButton
				:icon="house"
			/>
		</div>
		<div class="side-panel__avatars">
			<AvatarItem
				:src="avatar1"
			/>
			<AvatarItem
				:src="avatar2"
			/>
			<AvatarItem
				:src="avatar3"
			/>
			<AvatarItem
				:src="avatar4"
			/>
			<IconButton
			:icon="plus"
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
from '@/assets/js/icons.js'

import {
	avatar1,
	avatar2,
	avatar3,
	avatar4,
}
from '@/assets/js/avatars.js'

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