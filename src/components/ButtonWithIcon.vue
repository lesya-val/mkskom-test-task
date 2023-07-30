<template>
  <button class="button-with-icon">
		<span v-html="icon" class="icon"></span>
		<button class="button-with-icon__btn">{{ name }}</button>
	</button>
</template>

<script>

export default {
  name: "ButtonWithIcon",
	props: {
		icon:  {
			type: String,
      required: true,
		},
		name: {
			type: String,
      required: true,
		}
	}
};

</script>