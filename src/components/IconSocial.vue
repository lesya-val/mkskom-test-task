<template>
  <div class="icon-social">
		<img :src="iconSocial" alt="Social">
  </div>
</template>

<script>

export default {
  name: 'SocialMedia',
	props: {
		iconSocial: {
			type: String,
			required: true,
		},
	}
}
</script>