<template>
  <div :class="$style['sidebar-gallery']">
    <div :class="$style['sidebar-gallery__folders']">
      <ButtonWithIcon
				:class="[$style['sidebar-gallery__btn'], 'icon--translucent']"
        :icon="invoice"
        name="New Note"
      />
      <div :class="$style['sidebar-gallery__menu']">
        <IconAndTitle
          :class="$style['sidebar-gallery__all']"
          :icon="folder"
          title="All Notes"
          :number="43"
        />
        <div :class="$style['sidebar-gallery__list']">
          <IconAndTitle :icon="folder" title="Design" :number="23" />
          <IconAndTitle :icon="folder" title="Code Blocks" :number="15" />
          <IconAndTitle :icon="folder" title="Drafts" :number="18" />
          <IconAndTitle :icon="folder" title="Peoples Review" :number="21" />
          <IconAndTitle :icon="folder" title="Social" :number="43" />
          <IconAndTitle :icon="folder" title="Labels" :number="36" />
          <IconAndTitle :icon="folder" title="My Notes" :number="29" />
        </div>
        <IconAndTitle
          :class="$style['sidebar-gallery__add']"
          :icon="plus"
          title="Add Folder"
        />
      </div>
    </div>
    <div :class="$style['sidebar-gallery__labels']">
      <h3>Labels</h3>
      <div :class="$style['sidebar-gallery__list']">
        <IconAndTitle :class="$style['sidebar-gallery__label']" :icon="label" title="Notes" />
        <IconAndTitle :class="[$style['sidebar-gallery__label'], 'icon--orange']" :icon="label" title="Change Notes" />
        <IconAndTitle :class="[$style['sidebar-gallery__label'], 'icon--green']" :icon="label" title="From Family" />
        <IconAndTitle :class="[$style['sidebar-gallery__label'], 'icon--purple']" :icon="label" title="Imagium" />
        <IconAndTitle :class="$style['sidebar-gallery__label']" :icon="label" title="Work" />
        <IconAndTitle :class="$style['sidebar-gallery__label']" :icon="plus" title="New Label" />
      </div>
    </div>
  </div>
</template>

<script>

import ButtonWithIcon from '@/components/UI/ButtonWithIcon/ButtonWithIcon.vue'
import IconAndTitle from '@/components/IconAndTitle/IconAndTitle.vue'
import { invoice, folder, plus, label, } from '@/assets/js/icons.js'
import styles from '@/components/SidebarGallery/SidebarGallery.module.scss'

export default {
  name: "SidebarGallery",
  components: {
    ButtonWithIcon,
		IconAndTitle,
	},
	data() {
		return {
			invoice: invoice,
			folder: folder,
			plus: plus,
			label: label,
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>