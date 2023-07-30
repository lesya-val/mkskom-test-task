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

export default {
  name: 'SocialMedia',
	components: {
		IconSocial,
	},
	data() {
		return {
			phone: require('../assets/image/iconsSocial/phone.svg'),
			mail: require('../assets/image/iconsSocial/mail.svg'),
			reader: require('../assets/image/iconsSocial/reader.svg'),
			telegram: require('../assets/image/iconsSocial/telegram.svg'),
			whatsapp: require('../assets/image/iconsSocial/whatsapp.svg'),
		}
	}
}
</script>