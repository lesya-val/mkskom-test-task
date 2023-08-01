<template>
  <div :class="[$style['part-gallery']]">
    <EditGallery 
			:isFlexMode="isFlexMode" 
			@setFlexMode="setFlexMode" 
			@setGridMode="setGridMode"
		/>
    <div v-show="isFlexMode" :class="[$style['flex-gallery-container'], $style['part-gallery__list']]">
      <PhotoCard
        v-for="photo in photos" 
        :key="photo.id" 
        :src="photo.url" 
        :title="getFirstTwoWords(photo.title)"
        data="28.11.2045"
      />
    </div>
    <div v-show="!isFlexMode" :class="[$style['grid-gallery-container'], $style['part-gallery__list']]">
			<GridRow :photos="getPhotosByColumns(photos, 2, 0)" :columns="2" />
      <GridRow :photos="getPhotosByColumns(photos, 3, 2)" :columns="3" />
    </div>
  </div>	
</template>

<script>

import EditGallery from '@/components/EditGallery/EditGallery.vue'
import PhotoCard from '@/components/PhotoCard/PhotoCard.vue'
import GridRow from '@/components/GridRow/GridRow.vue';
import styles from '@/components/PartGallery/PartGallery.module.scss'

export default {
  name: "PartGallery",
  components: {
		EditGallery,
		PhotoCard,
		GridRow,
	},
	data() {
		return {
			photos: [],
			isFlexMode: true,
		}
	},
	async mounted() {
    await this.getImages();
  },
	methods: {
    async getImages() {
      try {
        const response = await fetch('https://jsonplaceholder.typicode.com/photos?_limit=16')
        if (!response.ok){
          throw new Error('Network response was not ok')
        }
        const data = await response.json()
        this.photos = data.map((photo) => ({
          id: photo.id,
          url: photo.url,
          title: this.getFirstTwoWords(photo.title),
        }));
      }
      catch (error) {
        console.error('Error fetching photos:', error);
      }
    },
    
    getFirstTwoWords(title) {
      const words = title.split(' ');
      return words.length >= 2 ? `${words[0]} ${words[1]}` : title;
    },

		setFlexMode() {
      this.isFlexMode = true;
    },
    setGridMode() {
      this.isFlexMode = false;
    },

		getPhotosByColumns(photos, columns, startIndex) {
      const endIndex = startIndex + columns;
      return photos.slice(startIndex, endIndex);
    },
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>