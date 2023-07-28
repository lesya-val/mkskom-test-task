<template>
	<div class="navigation__content">
		<IconButton :icon="burgerIcon"/>
	</div>
</template>

<script>

import IconButton from '@/components/UI/IconButton.vue'
import { burgerIcon } from '@/assets/js/icons.js';

export default {
	name: "NavigationContent",
	components: {
		IconButton,
	},
	data() {
		return {
			burgerIcon: burgerIcon,
		}
	}
};

</script>

<style lang="scss">
	
</style>