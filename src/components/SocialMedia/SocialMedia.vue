<template>
  <div :class="$style['social-media']">
    <IconSocial v-for="(icon, index) in socialIcons" :key="index" :icon="icon" />
  </div>
</template>

<script>
import IconSocial from '@/components/IconSocial/IconSocial.vue';
import { phone, mail, reader, telegram, whatsapp } from '@/assets/js/icons.js';
import styles from '@/components/SocialMedia/SocialMedia.module.scss';

export default {
  name: 'SocialMedia',
  components: {
    IconSocial,
  },
  data() {
    return {
      socialIcons: [phone, mail, reader, telegram, whatsapp],
    };
  },
  computed: {
    $style() {
      return styles;
    },
  },
};
</script>
