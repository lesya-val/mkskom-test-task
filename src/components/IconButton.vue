<template>
  <button 
		class="icon-button" 
		type="button" 
		@click="toggleColor">

		<span
			v-html="icon" class="icon">
		</span>
  </button>
</template>

<script>
export default {
  name: "IconButton",
  props: {
    icon: {
      type: String,
      required: true,
    },
  },
};
</script>