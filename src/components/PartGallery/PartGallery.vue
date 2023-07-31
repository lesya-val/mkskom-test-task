<template>
  <div :class="$style['part-gallery']">
    <EditGallery/>
    <div :class="$style['part-gallery__list']">
      <PhotoCard
				v-for="photo in photos" :key="photo.id" :src="photo.url" title="Shooting Stars" data="28.11.2045"
			/>
    </div>
  </div>
</template>

<script>

import EditGallery from '@/components/EditGallery/EditGallery.vue'
import PhotoCard from '@/components/PhotoCard/PhotoCard.vue'
import styles from '@/components/PartGallery/PartGallery.module.scss'

export default {
  name: "PartGallery",
  components: {
		EditGallery,
		PhotoCard,
	},
	data() {
		return {
			photos: []
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
					title: photo.title,
					date: photo.date,
				}));
			}
			catch (error) {
				console.error('Error fetching photos:', error);
			}
		},
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>