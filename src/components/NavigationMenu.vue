<template>
	<nav class="navigation__menu">
		<ul class="navigation__list">
			<li class="navigation__item">Dashboard</li>
			<li class="navigation__item">About Us</li>
			<li class="navigation__item">News</li>
			<li class="navigation__item">User Policy</li>
			<li class="navigation__item">Contacts</li>
		</ul>
		<span v-html="ellipsisMenu" />
	</nav>
</template>

<script>

export default {
	name: "NavigationMenu",
	props: {
    ellipsisMenu: {
      type: String,
      required: true,
    },
  },
};

</script>

<style lang="scss">
	.navigation {
		&__menu {
			display: flex;
			justify-content: center;
			align-items: center;
			column-gap: 25px;
		}

		&__list {
			display: flex;
			justify-content: center;
			align-items: center;
			column-gap: 25px;

			color: var(--gray-blue-grey-blue-70, #7d8fb3);
			font: var(--bold-bold-13, 700 13px/25px "Roboto", sans-serif);
		}
	}
</style>