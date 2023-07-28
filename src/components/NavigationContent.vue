<template>
	<div class="navigation__content">
		<div class="navigation__logo">
			<IconButton class="navigation__icon-button" :icon="burgerIcon"/>
			<h1 class="navigation__title">Constructor</h1>
		</div>
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
	.navigation {
		&__content {
			display: flex;
			align-items: center;
			justify-content: space-between;
			column-gap: 80px;
			padding: 25px;
		}

		&__logo {
			display: flex;
			align-items: center;
			justify-content: space-center;
			column-gap: 35px;
		}

		&__title {
			color: var(--gray-blue-grey-blue-50, #4d5e80);
			font: var(--bold-bold-18, 700 18px/30px "Roboto", sans-serif);
		}
	}
</style>