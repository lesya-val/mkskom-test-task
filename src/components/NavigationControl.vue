<template>
	<div class="navigation__control">
		<IconButton
			:iconButton="bell"
		/>
		<IconButton
			:iconButton="close"
		/>
	</div>
</template>

<script>

import IconButton from './UI/IconButton.vue';

import {
	bell,
	close
}
from '@/assets/js/icons.js'

export default {
	name: "NavigationControl",
	components: {
		IconButton,
	},
	data() {
		return {
			bell: bell,
			close: close,
		}
	}
};

</script>

<style lang="scss">
	.navigation {
		&__control {
			display: flex;
			gap: 10px;
		}
	}
</style>