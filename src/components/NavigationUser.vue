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

<style lang="scss">
	.navigation {
		&__user {
			display: flex;
			align-items: center;
			gap: 15px;
		}

		&__user-name {
			color: var(--gray-blue-grey-blue-60, #6b7a99);
			font: var(--bold-bold-13, 700 13px/25px "Roboto", sans-serif);
		}
	}
</style>