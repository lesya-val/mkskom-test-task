<template>
  <button 
		class="icon-button" 
		type="button" 
		@click="toggleColor">

		<img :src="iconButton" alt="Icon">
  </button>
</template>

<script>
export default {
  name: "IconButton",
  props: {
    iconButton: {
      type: String,
      required: true,
    },
  },
};
</script>