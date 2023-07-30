<template>
  <button 
		class="icon-button" 
		type="button" 
		@click="toggleColor">

		<span
			v-html="iconButton">
		</span>
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