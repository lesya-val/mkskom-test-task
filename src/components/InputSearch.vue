<template>
	<div class="input-search">
		<div class="input-search__icon-input">
			<div v-if="icon">
				<span
					v-html="icon" class="icon">
				</span>
			</div>
			<input
				class="input-search__input"
				type="text"
				:placeholder="currentPlaceholder"
				@input="handleInput"
			>
		</div>
		<button v-if="iconAfter" type="submit">
			<span
				v-html="iconAfter" class="icon">
			</span>
		</button>
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
		icon: {
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