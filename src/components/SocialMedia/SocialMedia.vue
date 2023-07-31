<template>
  <div :class="$style['social-media']">
    <IconSocial :icon="phone" />
    <IconSocial :icon="mail" />
    <IconSocial :icon="reader" />
    <IconSocial :icon="telegram" />
    <IconSocial :icon="whatsapp" />
  </div>
</template>

<script>

import IconSocial from '@/components/IconSocial/IconSocial.vue'
import { phone, mail, reader, telegram, whatsapp, } from '@/assets/js/icons.js'
import styles from '@/components/SocialMedia/SocialMedia.module.scss'

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
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>