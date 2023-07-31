<template>
  <div :class="$style['edit-gallery']">
    <div :class="$style['edit-gallery__btns']">
      <div :class="$style['edit-gallery__display']">
        <IconButton 
          :icon="flex" 
          :class="[$style['edit-gallery__btn'], $style['edit-gallery__btn--left']]"
          @click="setFlexMode"
        />
        <IconButton 
          :icon="grid" 
          :class="[$style['edit-gallery__btn'], $style['edit-gallery__btn--right']]"
          @click="setGridMode"
        />
      </div>
      <IconButton :icon="trash" :class="$style['edit-gallery__btn']"/>
    </div>
    <InputSearch :icon="search" :class="$style['edit-gallery__input']"/>
  </div>
</template>

<script>

import IconButton from '@/components/UI/IconButton/IconButton.vue'
import InputSearch from '@/components/UI/InputSearch/InputSearch.vue'
import { grid, flex, trash, search } from '@/assets/js/icons.js'
import styles from '@/components/EditGallery/EditGallery.module.scss'

export default {
  name: "EditGallery",
  components: {
		IconButton,
		InputSearch,
	},
	data() {
		return {
			grid: grid,
			flex: flex,
			trash: trash,
			search: search,
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
	methods: {
    setFlexMode() {
      this.$emit('setFlexMode')
    },
    setGridMode() {
      this.$emit('setGridMode')
    },
  },
};

</script>