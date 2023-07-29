<template>
	<div class="user">
		<span v-html="iconUser" />
		<h2 class="user__name">Clayton Santos</h2>
	</div>
</template>

<script>


export default {
	name: "NavigationUser",
	props: {
    iconUser: {
      type: String,
      required: true,
    },
  },
};

</script>