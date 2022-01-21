<template>
  <base-section 
    id="community-reasons" 
    class="container"
    leftStyle="col-12 col-lg-8"
    rightStyle="d-none d-lg-flex justify-content-center align-items-center"
  >
    <template v-slot:left-side >
      <h3 class="mb-0 section-title">Razones de hacer comunidad<br/>en Near México</h3>

      <div class="questions">
        <div class="question-container">
          <p class="question">¿Qué es NEAR?</p>
          <p class="answer">
            NEAR es un protocolo descentralizado que utiliza un mecanismo de consenso de Proof of Stake, 
            que permite participar como validador ó staker a cualquier usuario con una conexión a internet y hacer uso del protocolo por medio de un wallet digital en la web. 
            Lo cual facilita la adopción de una plataforma descentralizada para proveer soluciones blockchain a la región de habla hispana.
          </p>
        </div>

        <div class="question-container">
          <p class="question">¿Por que usar NEAR?</p>
          <p class="answer">
            Hace uso de Sharding para proveer de escabilidad al protocolo y las aplicaciones que corren sobre su cadena de bloques. 
            Lo cual permite que múltiples cadenas corran en simultáneo, reduciendo los costos de uso del protocolo. 
            Con esto los usuarios y desarrolladores pagan cuotas reducidas de gas al interactuar con las aplicaciones.
          </p>
        </div>

        <div class="question-container">
          <p class="question">¿Por que usar NEAR?</p>
          <p class="answer">
            NEAR Protocol es una solución de Capa 1, por lo cual tienes el respaldo de la Fundación NEAR que está apoyando el desarrollo del protocolo de código abierto y tiene un equipo detrás de NEAR inc que desarrollan las bases fundamentales para que el protocolo siga evolucionando bajo la custodia de la comunidad de NEAR; 
            la cual esta conformada de guilds (sindicatos) como NEAR Hispano.
          </p>
        </div>
      </div>
    </template>

    <template v-slot:right-side >
      <img width="236" height="356" src="~/assets/images/logo-lg.svg" alt="Logo de Near México" class="img-fluid">
    </template>
  </base-section>
</template>

<script>
export default {
  
}
</script>

<style scoped>
</style>