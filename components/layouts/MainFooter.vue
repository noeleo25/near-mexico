<template>
  <footer class="text-center">
    <img src="~/assets/images/logo.svg" width="128" height="46"/>
    <SocialMediaButtons class="social-media mx-auto"/>
    <p>Todos los derechos reservados ®2021, Prohibida su reproducción total o parcial sin autorización.</p>
  </footer>
</template>

<script>
import SocialMediaButtons from '@/components/buttons/SocialMediaButtons.vue'

export default {
  components: {
    SocialMediaButtons
  }
}
</script>

<style scoped>
footer {
  background-color: #2f2e41;
  margin-top: 180px;
  padding: 100px 0 22px;
}

.social-media {
  justify-content: center;
  max-width: 504px;
  margin: 22px 0px 62px;
}

p {
  color: #FFFFFF;
  font-size: 14px;
}
</style>