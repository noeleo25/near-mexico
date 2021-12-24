<template>
  <b-nav id="social-media-buttons">
    <b-nav-item 
      v-for="(sm, index) in socialMediaLinks"
      :key="index"
      :class="['social-media', sm.css]"
      :href="sm.networkLink"
      target="_blank"
    >
      <base-icon
        class="mr-2"
        :icon-name="sm.icon + '-icon'"
        height="24"
        width="24"
      >
        <component :is="sm.icon" />
      </base-icon>
      {{ sm.network }}
    </b-nav-item>
    
  </b-nav>
</template>

<script>
import FacebookIcon from '@/components/icons/FacebookIcon.vue'
import TelegramIcon from '@/components/icons/TelegramIcon.vue'
import TwitterIcon from '@/components/icons/TwitterIcon.vue'
import WhatsAppIcon from '@/components/icons/WhatsAppIcon.vue'
import GithubIcon from '@/components/icons/GithubIcon.vue'
import YoutubeIcon from '@/components/icons/YoutubeIcon.vue'


export default {
  components: {
    FacebookIcon,
    TelegramIcon,
    TwitterIcon,
    WhatsAppIcon,
    GithubIcon,
    YoutubeIcon
  },
  data() {
    return {
      socialMediaLinks: [
        {
          network: 'Telegram',
          networkLink: '#',
          icon: 'TelegramIcon',
          css: 'telegram'
        },
        {
          network: 'WhatsApp',
          networkLink: '#',
          icon: 'WhatsAppIcon',
          css: 'whatsapp'
        },
        {
          network: 'Twitter',
          networkLink: 'https://twitter.com/NearMexico',
          icon: 'TwitterIcon',
          css: 'twitter'
        },
        {
          network: 'Facebook',
          networkLink: 'https://www.facebook.com/NEAR.Mexico',
          icon: 'FacebookIcon',
          css: 'facebook'
        },
        {
          network: 'Github',
          networkLink: 'https://github.com/nearmexicooficial',
          icon: 'GithubIcon',
          css: 'github'
        },
        {
          network: 'Youtube',
          networkLink: 'https://www.youtube.com/channel/UCEBQEcQAh4UN33lmRd6qinw',
          icon: 'YoutubeIcon',
          css: 'youtube'
        }
      ]
    }
  },
}
</script>

<style scoped>
.social-media a {
  font-size: .88rem;
  font-weight: 600;
}

.telegram a {
  color: #269ed9;
}
.whatsapp a {
  color: #29c44d;
}
.twitter a {
  color: #1da1f2;
}
.facebook a {
  color: #1877f2;
}
.github a {
  color: #000000;
}
.youtube a {
  color: #FF0000;
}
</style>