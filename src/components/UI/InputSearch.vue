<template>
	<div class="input-search">
		<div class="input-search__icon-input">
			<button v-if="iconBefore" v-html="iconBefore"></button>
			<input
				class="input-search__input"
				type="text"
				:placeholder="currentPlaceholder"
				@input="handleInput"
			>
		</div>
		<button v-if="iconAfter" v-html="iconAfter" type="submit"></button>
	</div>
</template>

<script>

export default {
	name: "InputSearch",
	props: {
    currentPlaceholder: {
      type: String,
      default: "Search",
    },
		iconBefore: {
      type: String,
			default: "",
    },
		iconAfter: {
      type: String,
      default: "",
    },
		placeholderStyle: {
			type: Object,
      default: () => ({}),
		}
  },
	methods: {
		handleInput(event) {
			const inputValue = event.target.value;
			event.target.value = inputValue.replace(/\D/g, "");
		},
	},
};

</script>

<style lang="scss">
	.input-search{
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 10px;
		width: 100%;
		height: 30px;

		&__icon-input {
			display: flex;
			gap: 10px;
		}

		&__input {
			width: 200px;
		}

		&__input::placeholder {
			color: var(--gray-blue-grey-blue-80, #adb8cc);
			font: var(--bold-bold-12, 700 12px/20px "Roboto", sans-serif);
		}
	}
</style>