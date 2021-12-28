
<template>
  <base-section 
    id="community-near" 
    class="container"
    dividerRight
    leftStyle="d-none d-lg-block"
  >
    <template v-slot:left-side >
      <img width="402" height="300" src="~/assets/images/community-near.svg" alt="Illustration good team" class="img-fluid">
    </template>

    <template v-slot:right-side >
      <h2 class="mb-0 section-title">Comunidad de Near México</h2>
      <p class="text-justify">
        Somos un grupo de entusiastas Mexicanos conformados por 
        distintos perfiles profesionales: creadores, colaboradores, 
        emprendedores e iniciales los cuales tenemos como objetivo la 
        difusión y apoyo en el trabajo de la tecnología blockchain.
      </p>

      <p class="text-justify">
        Si quieres pasar un buen rato compartiendo y aprendiendo 
        conocimiento  te invitamos a unirte a esta gran comunidad. 
      </p>

      <SocialMediaButtons class="social-media mx-auto"/>
    </template>
  </base-section>
</template>

<script>
import SocialMediaButtons from '@/components/buttons/SocialMediaButtons.vue';
export default {
  components: {
    SocialMediaButtons
  }
}
</script>

<style scoped>
.right-col p {
  margin-bottom: 2rem;
}

.social-media {
  max-width: 540px;
  justify-content: center;
}

</style>