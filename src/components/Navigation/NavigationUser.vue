<template>
	<div class="navigation__user">
		<span v-html="iconUser" />
		<h2 class="navigation__user-name">Clayton Santos</h2>
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