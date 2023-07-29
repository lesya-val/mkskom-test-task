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
import NavigationMenu from '@/components/NavigationMenu.vue'
import InputSearch from '@/components/UI/InputSearch.vue'
import NavigationInfo from '@/components/NavigationInfo.vue'

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

<style lang="scss">
	.navigation {
		border-bottom: solid 2px var(--gray-blue-grey-blue-95, #edeff2);
		
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

		&__input {
			display: flex;
			align-items: center;
			background: var(--white-white, #ffffff);
			border-radius: 30px ;
			border: 2px solid var(--gray-blue-grey-blue-97, #f5f6f7);
			padding: 20px 15px;
			width: 430px;
			height: 50px;
		}
	}
</style>