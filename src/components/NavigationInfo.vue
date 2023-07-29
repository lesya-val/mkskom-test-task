<template>
	<div class="navigation__info">
		<NavigationUser
			:iconUser="user"
		/>
		<NavigationControl/>
	</div>
</template>

<script>

import NavigationUser from './NavigationUser.vue'
import NavigationControl from './NavigationControl.vue'

import { 
	user,
}
from '@/assets/js/icons.js'

export default {
	name: "NavigationInfo",
	components: {
		NavigationUser,
		NavigationControl,
	},

	data() {
		return {
			user: user,
		}
	}
};

</script>

<style lang="scss">
	.navigation {
		&__info {
			display: flex;
			gap: 30px;
		}
	}
</style>