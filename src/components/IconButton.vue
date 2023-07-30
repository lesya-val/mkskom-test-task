<template>
  <button 
		class="icon-button" 
		type="button" 
		@click="toggleColor"
		v-html="iconButton">
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