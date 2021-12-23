<template>
  <b-nav id="social-media-buttons">
    <b-nav-item class="social-media telegram">
      <base-icon
        class="mr-2"
        icon-name="telegram-icon"
        height="24"
        width="24"
      >
        <TelegramIcon/>
      </base-icon>
      Telegram
    </b-nav-item>
    <b-nav-item class="social-media whatsapp">
      <base-icon
        class="mr-2"
        icon-name="whatsapp-icon"
        height="24"
        width="24"
      >
        <WhatsAppIcon/>
      </base-icon>
      WhatsApp
    </b-nav-item>
    <b-nav-item class="social-media twitter">
      <base-icon
        class="mr-2"
        icon-name="twitter-icon"
        height="24"
        width="24"
      >
        <TwitterIcon/>
      </base-icon>
      Twitter
    </b-nav-item>
    <b-nav-item class="social-media facebook">
      <base-icon
        class="mr-2"
        icon-name="facebook-icon"
        height="24"
        width="24"
      >
        <FacebookIcon/>
      </base-icon>
      Facebook
    </b-nav-item>
  </b-nav>
</template>

<script>
import FacebookIcon from '@/components/icons/FacebookIcon.vue'
import TelegramIcon from '@/components/icons/TelegramIcon.vue'
import TwitterIcon from '@/components/icons/TwitterIcon.vue'
import WhatsAppIcon from '@/components/icons/WhatsAppIcon.vue'

export default {
  components: {
    FacebookIcon,
    TelegramIcon,
    TwitterIcon,
    WhatsAppIcon
  }
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
</style>