<template>
  <div class="social-media">
		<IconSocial
			:iconSocial="phone"
		/>
		<IconSocial
			:iconSocial="mail"
		/>
		<IconSocial
			:iconSocial="reader"
		/>
		<IconSocial
			:iconSocial="telegram"
		/>
		<IconSocial
			:iconSocial="whatsapp"
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
from '@/assets/js/iconsSocial'

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