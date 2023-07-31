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
      <span v-html="icon" :class="$style['icon']"></span>
    </button>
  </nav>
</template>

<script>

import styles from '@/components/MenuList/MenuList.module.scss'

export default {
	name: "MenuList",
	props: {
    icon: {
      type: String,
      required: true,
    },
  },
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>