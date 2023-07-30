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
				<UserInfo 
					:iconUser="user"
					:name="name"
				/>
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

import IconButton from '@/components/IconButton.vue'
import MenuList from '@/components/MenuList.vue'
import InputSearch from '@/components/InputSearch.vue'
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

from '@/assets/js/iconsButton.js'

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
			name: 'Clayton Santos',
		}
	}
};

</script>