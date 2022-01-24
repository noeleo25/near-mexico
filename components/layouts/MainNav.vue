<template>
  <b-navbar 
    type="dark"
    class="py-4"
  >
    <b-container class="d-flex flex-column flex-md-row">
      
      <b-navbar-brand href="#" class="py-2">
        <NearLogo/>
      </b-navbar-brand>

      <b-navbar-nav class="mx-auto d-none d-md-block">
        <SwitchModeBtn/>
      </b-navbar-nav>

      <b-navbar-nav class="mx-auto mt-2 mt-md-0 ml-lg-auto mr-lg-5">
        <li class="nav-li link-box">
          <nuxt-link to="/">
            Inicio
          </nuxt-link>
        </li>
        <li class="nav-li link-box mx-3">
          <nuxt-link to="#community-near">
            Nosotros
          </nuxt-link>
        </li>
        <li class="nav-li link-box">
          <nuxt-link to="#news">
            Noticias
          </nuxt-link>
        </li>
      </b-navbar-nav>

      <b-navbar-nav class="d-none d-lg-flex">
        <li class="nav-li link-box mr-0 mr-lg-4 mt-3 mt-lg-0">
          <nuxt-link 
            to="/" 
            class="d-flex link-to-tg"
          >
            <base-icon
              class="mr-2"
              icon-name="telegram-icon"
            >
              <TelegramIcon/>
            </base-icon>
            Telegram
          </nuxt-link>
        </li>

        <li class="nav-li link-box mr-0 mr-lg-4 mt-3 mt-lg-0">
          <nuxt-link 
            to="/" 
            class="d-flex link-to-ws"
          >
            <BaseIcon
              class="mr-2"
              icon-name="whatsapp-icon"
            >
              <WhatsAppIcon/>
            </BaseIcon>
            Whatsapp
          </nuxt-link>
        </li>
      </b-navbar-nav>

    </b-container>
  </b-navbar>
</template>

<script>
import TelegramIcon from '@/components/icons/TelegramIcon.vue'
import WhatsAppIcon from '@/components/icons/WhatsAppIcon.vue'

import NearLogo from '@/components/images/NearLogoImg.vue'

import SwitchModeBtn from '@/components/buttons/SwitchModeBtn.vue'
export default {
  components: {
    TelegramIcon,
    WhatsAppIcon,
    NearLogo,
    SwitchModeBtn
  }
}
</script>

<style scoped>
.navbar-nav .nav-li {
  align-items: center;
  display: flex;
  width: 100%;
  justify-content: flex-start;
  flex-basis: 1%;
}

.nav-li a {
  color: var(--primary-color);
  font-size: .95rem;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  width: 100%;
  text-align: center;
}

.nav-li .link-to-tg {
  color: #269ed9;
}

.nav-li .link-to-ws {
  color: #29c44d;
}


.link-box > a {
  padding: 10px;
  position: relative;
  font-weight: normal;
  transition: font-weight 0.5s ease;
}

.link-box > a:hover {
  text-decoration: none;
}

.link-box > a:after,
.link-box > a.router-link-active:after {
  content: "";
  transition: 0.5s all ease;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  position: absolute;
  bottom: 0;
  left: 0;
  background: var(--primary-color);
  height: 4px;
  width: 0;
}

.link-box > a:hover:after,
.link-box > a.router-link-active:after {
  width: 100%;
}

@media (min-width: 992px) {
  .navbar-nav .nav-li {
    flex-grow: 0;
    flex-shrink: 0;
    flex-basis: 20%;
    margin-bottom: 0;
    justify-content: center;
  }

  .nav-li a {
    width: auto;
    text-align: center;
  }
}
</style>