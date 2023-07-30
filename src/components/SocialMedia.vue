<template>
  <div class="social-media">
		<IconSocial
			:icon="phone"
		/>
		<IconSocial
			:icon="mail"
		/>
		<IconSocial
			:icon="reader"
		/>
		<IconSocial
			:icon="telegram"
		/>
		<IconSocial
			:icon="whatsapp"
		/>
  </div>
</template>

<script>

import IconSocial from '@/components/IconSocial.vue'

import {
	phone,
	mail,
	reader,
	telegram,
	whatsapp,
}
from '@/assets/js/icons.js'

export default {
  name: 'SocialMedia',
	components: {
		IconSocial,
	},
	data() {
		return {
			phone: phone,
			mail: mail,
			reader: reader,
			telegram: telegram,
			whatsapp: whatsapp,
		}
	}
}
</script>