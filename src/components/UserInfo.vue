<template>
	<div class="user">
		<div class="user__img">
			<span
				v-html="icon">
			</span>
		</div>
		<h2 class="user__name">{{ name }}</h2>
	</div>
</template>

<script>


export default {
	name: "NavigationUser",
	props: {
    icon: {
      type: String,
      required: true,
    },
		name: {
			type: String,
      required: true,
		}
  },
};

</script>