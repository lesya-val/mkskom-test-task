<template>
  <div :class="$style['navigation']">
    <div :class="$style['navigation__content']">
      <div :class="$style['navigation__logo']">
        <IconButton :class="$style['navigation__icon-button']" :icon="burger" />
        <h1 :class="$style['navigation__title']">Constructor</h1>
      </div>
      <MenuList :icon="ellipsis" />
      <div :class="$style['navigation__input']">
        <InputSearch
          :currentPlaceholder="currentPlaceholder"
          :icon="search"
          :iconAfter="arrow"
        />
      </div>
      <div :class="$style['navigation__info']">
        <UserInfo :icon="user" :name="name" />
        <div :class="$style['navigation__control-btns']">
          <IconButton :icon="bell" />
          <IconButton :icon="close" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import IconButton from '@/components/UI/IconButton/IconButton.vue'
import MenuList from '@/components/MenuList/MenuList.vue'
import InputSearch from '@/components/UI/InputSearch/InputSearch.vue'
import UserInfo from '@/components/UserInfo/UserInfo.vue'

import { burger, search, arrow, ellipsis, user, bell, close, } from '@/assets/js/icons.js'

import styles from '@/components/NavigationBar/NavigationBar.module.scss'

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
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>