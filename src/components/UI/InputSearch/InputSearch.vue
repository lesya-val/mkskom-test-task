<template>
	<div :class="$style['input-search']">
    <div :class="$style['input-search__icon-input']">
      <div>
        <span v-html="icon"></span>
      </div>
      <input
        :class="$style['input-search__input']"
        type="text"
        :placeholder="placeholder"
        @input="handleInput"
      >
    </div>
    
  </div>
</template>

<script>

import styles from '@/components/UI/InputSearch/InputSearch.module.scss'

export default {
	name: "InputSearch",
	props: {
    placeholder: {
      type: String,
      default: "Search",
    },
		icon: {
      type: String,
			default: "",
    },
		numberValidate: {
      type: Boolean,
      default: false,
    },
  },
	methods: {
		handleInput(event) {
      const inputValue = event.target.value;
      if (this.numberValidate) {
        event.target.value = inputValue.replace(/\D/g, "");
      }
    },
	},
	computed: {
    $style() {
      return styles;
    },
  },
};

</script>