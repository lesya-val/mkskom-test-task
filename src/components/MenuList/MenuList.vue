<template>
  <nav :class="$style['menu']">
    <ul :class="$style['menu__list']">
      <li v-for="(item, index) in menuItems" :key="index" :class="$style['menu__item']">
        {{ item.text }}
      </li>
    </ul>
    <button>
      <IconItem :icon="ellipsis" />
    </button>
  </nav>
</template>

<script>
import IconItem from '@/components/UI/IconItem/IconItem.vue';
import { ellipsis } from '@/assets/js/icons.js';
import styles from '@/components/MenuList/MenuList.module.scss';

export default {
  name: "MenuList",
  components: {
    IconItem,
  },
  data() {
    return {
      ellipsis: ellipsis,
      menuItems: [
        { text: "Dashboard" },
        { text: "About Us" },
        { text: "News" },
        { text: "User Policy" },
        { text: "Contacts" },
      ],
    };
  },
  computed: {
    $style() {
      return styles;
    },
  },
};
</script>