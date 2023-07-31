<template>
	<nav :class="$style['menu']">
    <ul :class="$style['menu__list']">
      <li :class="$style['menu__item']">Dashboard</li>
      <li :class="$style['menu__item']">About Us</li>
      <li :class="$style['menu__item']">News</li>
      <li :class="$style['menu__item']">User Policy</li>
      <li :class="$style['menu__item']">Contacts</li>
    </ul>
    <button>
      <IconItem :icon="ellipsis"/>
    </button>
  </nav>
</template>

<script>

import IconItem from '@/components/UI/IconItem/IconItem.vue'
import { ellipsis } from '@/assets/js/icons.js'
import styles from '@/components/MenuList/MenuList.module.scss'

export default {
	name: "MenuList",
	components: {
		IconItem,
	},
	props: {
    icon: {
      type: String,
      required: true,
    },
  },
	data() {
		return {
			ellipsis: ellipsis,
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>