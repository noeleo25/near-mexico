
<template>
  <base-section 
    id="main-banner" 
    leftStyle="text-col d-flex flex-column justify-content-center"
    rightStyle="img-col d-none d-lg-block"
  >
    <template v-slot:left-side >
      <h1 class="mb-0"><span class="text-uppercase">Near</span> México</h1>
      <p>La voz de la comunidad para el ecosistema NEAR en México</p>
      <div>
        <button class="join-btn mr-2">Unirse</button>
        <button class="welcome-btn">
          Bienvenida
          <base-icon
            class="ml-1"
            icon-name="whatsapp-icon"
          >
            <PlayIcon/>
          </base-icon>
        </button>
      </div>
    </template>

    <template v-slot:right-side >
      <img width="506" height="442" src="~/assets/images/mexico-banner.svg" alt="Mexico's map">
    </template>
  </base-section>
</template>

<script>
import PlayIcon from '@/components/icons/PlayIcon.vue';
export default {
  components: {
    PlayIcon
  },
}
</script>

<style scoped>
.text-col h1 {
  font-size: 3.5rem;
  font-weight: 800;
}
.text-col p {
  font-size: 1rem;
  font-weight: 600;
}
.text-col .join-btn {
  width: 116px;
  height: 42px;
  border: 0;
  border-radius: 6px;
  box-shadow: 0 3px 6px 0 rgba(0, 0, 0, 0.16);
  background-color: #29c44d;
  font-size: 1rem;
  color: #FFFFFF;
}
.text-col .welcome-btn {
  width: 140px;
  height: 42px;
  border-radius: 6px;
  border: solid 1px #29c44d;
  background-color: transparent;
  color: #29c44d;
}
</style>