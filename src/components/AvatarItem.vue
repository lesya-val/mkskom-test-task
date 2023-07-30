<template>
  <button class="avatar">
		<img :src="src" alt="Avatar">
	</button>
</template>

<script>

export default {
  name: 'AvatarItem',
	props: {
		src: {
      type: String,
      required: true,
    },
	}
}
</script>