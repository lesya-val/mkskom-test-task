<template>
  <div class="navigation">
		<div class="navigation__content">
			<div class="navigation__logo">
				<IconButton class="navigation__icon-button" :iconButton="burger"/>
				<h1 class="navigation__title">Constructor</h1>
			</div>
			<MenuList
				:ellipsisMenu="ellipsis"
			/>
			<div class="navigation__input">
				<InputSearch
					:currentPlaceholder = currentPlaceholder
					:iconBefore = "search"
					:iconAfter="arrow"
				/>
			</div>
			<div class="navigation__info">
				<UserInfo :iconUser="user"/>
				<div class="navigation__control-btns">
					<IconButton
					:iconButton="bell"
					/>
					<IconButton
						:iconButton="close"
					/>
				</div>
			</div>
		</div>
  </div>
</template>

<script>

import IconButton from '@/components/UI/IconButton.vue'
import MenuList from '@/components/MenuList.vue'
import InputSearch from '@/components/UI/InputSearch.vue'
import UserInfo from '@/components/UserInfo.vue'

import { 
	burger,
	search,
	arrow,
	ellipsis,
	user,
	bell,
	close,
} 

from '@/assets/js/icons.js'

export default {
	name: "NavigationBar",
	components: {
		IconButton,
		MenuList,
		InputSearch,
		UserInfo,
	},
	data() {
		return {
			burger: burger,
			search: search,
			arrow: arrow,
			ellipsis: ellipsis,
			user: user,
			bell: bell,
			close: close,
			currentPlaceholder: "Search Transactions and Documents",
		}
	}
};

</script>