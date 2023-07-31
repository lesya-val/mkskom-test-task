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
        :title="photo.title"
        data="28.11.2045"
      />
    </div>
    <div v-show="!isFlexMode" :class="[$style['grid-gallery-container'], $style['part-gallery__list']]">
			<GridRowTwo :photos="photoRows1" />
      <GridRowThree :photos="photoRows2" />
			<GridRowTwo :photos="photoRows3" />
      <GridRowThree :photos="photoRows4" />
			<GridRowTwo :photos="photoRows5" />
      <GridRowThree :photos="photoRows6" />
    </div>
  </div>
</template>

<script>

import EditGallery from '@/components/EditGallery/EditGallery.vue'
import PhotoCard from '@/components/PhotoCard/PhotoCard.vue'
import GridRowTwo from '@/components/GridRowTwo/GridRowTwo.vue';
import GridRowThree from '@/components/GridRowThree/GridRowThree.vue';
import styles from '@/components/PartGallery/PartGallery.module.scss'

export default {
  name: "PartGallery",
  components: {
		EditGallery,
		PhotoCard,
		GridRowTwo,
		GridRowThree,
	},
	data() {
		return {
			photos: [],
			isFlexMode: true,
		}
	},
	created() {
    this.getImages();
  },
	methods: {
		async getImages() {
			try {
				const responce = await fetch('https://jsonplaceholder.typicode.com/photos?_limit=16')
				if (!responce.ok){
					throw new Error('Network response was not ok')
				}
				const data = await responce.json()
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
			if (words.length >= 2) {
				return `${words[0]} ${words[1]}`;
			} else {
				return title;
			}
		},

		setFlexMode() {
      this.isFlexMode = true;
    },
    setGridMode() {
      this.isFlexMode = false;
    },
	},
	computed: {
    $style() {
      return styles;
    },
		photoRows1() {
      return this.photos.slice(0, 2);
    },
    photoRows2() {
      return this.photos.slice(2, 5);
    },
		photoRows3() {
      return this.photos.slice(5, 7);
    },
		photoRows4() {
      return this.photos.slice(7, 10);
    },
		photoRows5() {
      return this.photos.slice(10, 12);
    },
		photoRows6() {
      return this.photos.slice(12, 15);
    },
  },
};

</script>