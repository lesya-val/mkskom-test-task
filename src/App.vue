<template>
	<MainPage/>
</template>

<script>

import MainPage from '@/pages/MainPage.vue'

export default {
  name: 'App',
  components: {
    MainPage,
  }
}
</script>

<style lang="scss">
	#app {
		background: var(--gray-blue-grey-blue-98, #f7f8fa);
		max-width: 1600px;
		height: 100%;
		margin: 0 auto;

		color: var(--gray-blue-grey-blue-60, #6b7a99);
		font: var(--bold-bold-12, 700 12px/20px "Roboto", sans-serif);
	}
</style>
