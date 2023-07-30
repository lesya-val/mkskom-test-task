<template>
	<div class="user">
		<div class="user__img">
			<img :src="iconUser" alt="User">
		</div>
		<h2 class="user__name">{{ name }}</h2>
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
		name: {
			type: String,
      required: true,
		}
  },
};

</script>