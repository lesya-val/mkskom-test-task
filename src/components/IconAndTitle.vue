<template>
  <div class="icon-and-title">
		<div class="icon-and-title__title">
			<span v-html="icon" class="icon"></span>
			<h3>{{ title }}</h3>
		</div>
		<p>{{ number }}</p>
	</div>
</template>

<script>

export default {
  name: "IconAndTitle",
  components: {
    
	},
	props: {
		icon: {
			type: String,
			required: true,
		},
		title: {
			type: String,
			required: true,
		},
		number: {
			type: Number,
			required: false,
		},
	},
};

</script>