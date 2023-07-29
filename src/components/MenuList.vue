<template>
	<nav class="menu">
		<ul class="menu__list">
			<li class="menu__item">Dashboard</li>
			<li class="menu__item">About Us</li>
			<li class="menu__item">News</li>
			<li class="menu__item">User Policy</li>
			<li class="menu__item">Contacts</li>
		</ul>
		<span v-html="ellipsisMenu" />
	</nav>
</template>

<script>

export default {
	name: "MenuList",
	props: {
    ellipsisMenu: {
      type: String,
      required: true,
    },
  },
};

</script>