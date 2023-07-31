<template>
  <div class="photo-card">
    <div class="photo-card__img">
			<img :src="src">
		</div>
		<div class="photo-card__info">
			<h3 class="photo-card__title">{{ title }}</h3>
			<p class="photo-card__data"> {{ data }}</p>
		</div>
  </div>
</template>

<script>

import styles from '@/components/PhotoCard/PhotoCard.module.scss'

export default {
  name: "PhotoCard",
  components: {
		
	},
	props: {
		src: {
			type : String,
			require: true,
		},
		title: {
			type : String,
			require: true,
		},
		data: {
			type : String,
			require: true,
		},
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>

<style lang="scss">
	.photo-card {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 20px;
		max-width: 160px;

		&__img {
			padding: 5px;
		}

		&__img img {
			max-height: 110px;
		}

		&__info {
			display: flex;
			flex-direction: column;
			align-items: center;
			gap: 10px;
		}

		&__title {
			color: var(--gray-blue-grey-blue-60, #6b7a99);
			font: var(--bold-bold-12, 700 12px/20px "Roboto", sans-serif);
		}

		&__data {
			color: var(--gray-blue-grey-blue-70, #7d8fb3);
			font: var(--black-black-10, 900 10px/20px "Roboto", sans-serif);
		}
}

</style>