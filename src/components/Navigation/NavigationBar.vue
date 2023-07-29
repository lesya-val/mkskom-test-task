<template>
  <div class="navigation">
		<div class="navigation__content">
			<div class="navigation__logo">
				<IconButton class="navigation__icon-button" :iconButton="burger"/>
				<h1 class="navigation__title">Constructor</h1>
			</div>
			<NavigationMenu
				:ellipsisMenu="ellipsis"
			/>
			<div class="navigation__input">
				<InputSearch
					:currentPlaceholder = currentPlaceholder
					:iconBefore = "search"
					:iconAfter="arrow"
				/>
			</div>
			<NavigationInfo/>
		</div>
  </div>
</template>

<script>

import IconButton from '@/components/UI/IconButton.vue'
import NavigationMenu from '@/components/Navigation/NavigationMenu.vue'
import InputSearch from '@/components/UI/InputSearch.vue'
import NavigationInfo from '@/components/Navigation/NavigationInfo.vue'

import { 
	burger,
	search,
	arrow,
	ellipsis,
} 

from '@/assets/js/icons.js'

export default {
	name: "NavigationBar",
	components: {
		IconButton,
		NavigationMenu,
		InputSearch,
		NavigationInfo,
	},
	data() {
		return {
			burger: burger,
			search: search,
			arrow: arrow,
			ellipsis: ellipsis,
			currentPlaceholder: "Search Transactions and Documents",
		}
	}
};

</script>