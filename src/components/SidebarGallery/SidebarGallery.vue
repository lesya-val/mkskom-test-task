<template>
  <div :class="$style['sidebar-gallery']">
    <div :class="$style['sidebar-gallery__folders']">
      <ButtonWithIcon
        :class="[$style['sidebar-gallery__btn'], 'icon--translucent']"
        :icon="invoice"
        name="New Note"
      />
      <SidebarGalleryMenu />
      <IconAndTitle
        :class="$style['sidebar-gallery__add']"
        :icon="plus"
        title="Add Folder"
      />
    </div>
    <SidebarGalleryLabels />
  </div>
</template>

<script>
import ButtonWithIcon from '@/components/UI/ButtonWithIcon/ButtonWithIcon.vue';
import SidebarGalleryMenu from '@/components/SidebarGalleryMenu/SidebarGalleryMenu.vue';
import SidebarGalleryLabels from '@/components/SidebarGalleryLabels/SidebarGalleryLabels.vue';
import IconAndTitle from '@/components/IconAndTitle/IconAndTitle.vue';
import { invoice, plus } from '@/assets/js/icons.js';
import styles from '@/components/SidebarGallery/SidebarGallery.module.scss';

export default {
  name: "SidebarGallery",
  components: {
    ButtonWithIcon,
    SidebarGalleryMenu,
    SidebarGalleryLabels,
    IconAndTitle,
  },
  data() {
    return {
      invoice: invoice,
      plus: plus,
    };
  },
  computed: {
    $style() {
      return styles;
    },
  },
};
</script>
