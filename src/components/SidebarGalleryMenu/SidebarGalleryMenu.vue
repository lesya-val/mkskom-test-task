<template>
  <div :class="$style['sidebar-gallery__menu']">
    <IconAndTitle
      :class="$style['sidebar-gallery__all']"
      :icon="folder"
      title="All Notes"
      :number="43"
    />
    <div :class="$style['sidebar-gallery__list']">
      <div v-for="(menuItem, index) in menuItems" :key="index" :class="$style['sidebar-gallery__item']">
        <IconAndTitle :icon="menuItem.icon" :title="menuItem.title" :number="menuItem.number" />
      </div>
    </div>
  </div>
</template>

<script>
import IconAndTitle from '@/components/IconAndTitle/IconAndTitle.vue';
import { folder, plus } from '@/assets/js/icons.js';
import styles from '@/components/SidebarGalleryMenu/SidebarGalleryMenu.module.scss';

export default {
  name: "SidebarGalleryMenu",
  components: {
    IconAndTitle,
  },
  data() {
    return {
      folder: folder,
      plus: plus,
      menuItems: [
        { icon: folder, title: "Design", number: 23 },
        { icon: folder, title: "Code Blocks", number: 15 },
        { icon: folder, title: "Drafts", number: 18 },
        { icon: folder, title: "Peoples Review", number: 21 },
        { icon: folder, title: "Social", number: 43 },
        { icon: folder, title: "Labels", number: 36 },
        { icon: folder, title: "My Notes", number: 29 },
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
