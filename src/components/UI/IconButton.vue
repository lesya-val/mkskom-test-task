<template>
  <button class="icon-button" type="button" @click="toggleColor">
    <span v-html="currentIcon" />
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
  data() {
    return {
      currentIcon: this.iconButton,
      isColored: false,
    };
  },
  methods: {
    toggleColor() {
      this.isColored = !this.isColored;
      this.currentIcon = this.isColored ? this.getColoredIcon() : this.iconButton;
    },
    getColoredIcon() {
      return this.iconButton.replace(/fill="#C3CAD9"/g, 'fill="#FF6633"');
    },
  },
};
</script>

<style lang="scss">
  .icon-button {
    background: var(--white-white, #ffffff);
		border-radius: 100px;
		padding: 10px;
		box-shadow: var(
			--shadows-gray-blue-30-3-5-b-box-shadow,
			0px 2px 5px 0px rgba(38, 51, 77, 0.03)
		);
  }
</style>
