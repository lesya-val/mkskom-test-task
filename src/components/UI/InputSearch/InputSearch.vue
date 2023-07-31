<template>
	<div :class="$style['input-search']">
    <div :class="$style['input-search__icon-input']">
      <div v-if="icon">
        <span v-html="icon" :class="$style['icon']"></span>
      </div>
      <input
        :class="$style['input-search__input']"
        type="text"
        :placeholder="currentPlaceholder"
        @input="handleInput"
      >
    </div>
    <button v-if="iconAfter" type="submit">
      <span v-html="iconAfter" :class="$style['icon']"></span>
    </button>
  </div>
</template>

<script>

import styles from '@/components/UI/InputSearch/InputSearch.module.scss'

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
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>