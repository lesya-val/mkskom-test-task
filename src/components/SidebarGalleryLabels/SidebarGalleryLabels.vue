<template>
  <div :class="$style['sidebar-gallery__labels']">
    <h3>Labels</h3>
    <div :class="$style['sidebar-gallery__list']">
      <div v-for="(labelItem, index) in labelItems" :key="index" :class="$style['sidebar-gallery__label']">
        <IconAndTitle :icon="labelItem.icon" :title="labelItem.title" :class="[$style['sidebar-gallery__label'], labelItem.colorClass]"/>
      </div>
      <IconAndTitle :class="$style['sidebar-gallery__label']" :icon="plus" title="New Label" />
    </div>
  </div>
</template>

<script>
import IconAndTitle from '@/components/IconAndTitle/IconAndTitle.vue';
import { label, plus } from '@/assets/js/icons.js';
import styles from '@/components/SidebarGalleryLabels/SidebarGalleryLabels.module.scss';

export default {
  name: "SidebarGalleryLabels",
  components: {
    IconAndTitle,
  },
  data() {
    return {
      label: label,
      plus: plus,
      labelItems: [
        { icon: label, title: 'Notes', colorClass: '' },
        { icon: label, title: 'Change Notes', colorClass: 'icon--orange' },
        { icon: label, title: 'From Family', colorClass: 'icon--green' },
        { icon: label, title: 'Imagium', colorClass: 'icon--purple' },
        { icon: label, title: 'Work', colorClass: '' },
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
