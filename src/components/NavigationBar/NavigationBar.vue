<template>
  <div :class="$style['navigation']">
    <div :class="$style['navigation__content']">
      <div :class="$style['navigation__logo']">
        <IconButton :class="$style['navigation__icon-button']" :icon="burger" :isActive="index === activeIcon"
        @click="handleIconButton(index)"/>
        <h1 :class="$style['navigation__title']">Constructor</h1>
      </div>
      <MenuList/>
      <div :class="$style['navigation__input']">
        <InputSearch
					:class="$style['navigation__input-input']"
          :placeholder="currentPlaceholder"
          :icon="search"
					:iconAfter="arrow"
					numberValidate="shouldValidate"
					@searchAlbum="handleSearchAlbum"
        />
      </div>
      <div :class="$style['navigation__info']">
        <UserInfo :name="name" />
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
import { burger, search, arrow, bell, close, } from '@/assets/js/icons.js'
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
			bell: bell,
			close: close,
			currentPlaceholder: "Search Transactions and Documents",
			name: 'Clayton Santos',
			shouldValidate: true,
			activeIcon: null,
		}
	},
	methods: {
		handleSearchAlbum(albumId) {
			this.$emit("searchAlbum", albumId);
		},
		handleIconButton(index) {
			this.activeIcon = index;
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>