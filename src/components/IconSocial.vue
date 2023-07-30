<template>
  <div class="icon-social">
		<span 
			v-html="iconSocial">
		</span>
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