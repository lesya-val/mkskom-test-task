<template>
	<div class="navigation__info">
		<NavigationUser
			:iconUser="user"
		/>
		<NavigationControl/>
	</div>
</template>

<script>

import NavigationUser from '@/components/Navigation/NavigationUser.vue'
import NavigationControl from '@/components/Navigation/NavigationControl.vue'

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