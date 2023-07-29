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