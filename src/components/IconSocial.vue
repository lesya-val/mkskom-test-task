<template>
  <div class="icon-social">
		<span 
			v-html="icon" class="icon">
		</span>
  </div>
</template>

<script>

export default {
  name: 'SocialMedia',
	props: {
		icon: {
			type: String,
			required: true,
		},
	}
}
</script>