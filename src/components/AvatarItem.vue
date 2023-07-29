<template>
  <button class="avatar">
		<img :src="avatarSrc" alt="Avatar">
	</button>
</template>

<script>

export default {
  name: 'AvatarItem',
	props: {
		avatarSrc: {
      type: String,
      required: true,
    },
	}
}
</script>