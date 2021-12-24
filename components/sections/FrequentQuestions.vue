<template>
  <base-section 
    id="frequent-questions"
    leftStyle="col-12 col-lg-8"
    rightStyle="d-none d-lg-flex justify-content-end align-items-end"
    noDivider
  >
    <template v-slot:left-side >
      <h5 class="mb-0 section-title">Preguntas frecuentes</h5>

      <p class="question">¿Donde se reúnen los miembros de NEAR México?</p>
      <p class="answer">
        Por ahora estamos en el grupo de Telegram - NEAR Hispano y hacemos un meetup mensual en nuestro canal de Youtube.
      </p>
      
      <p class="question">¿Tiene algún costo formar parte del sindicato?</p>
      <p class="answer">
        Educar a la comunidad de habla hispana sobre el potencial del protocolo NEAR y canalizar ayudas de la fundación a los proyectos o miembros que contribuyen al crecimiento y/o adopción de NEAR en su localidad/región. 
        Apoyar con accesos a grants (subsidios) que ofrece la Fundación NEAR. 
        Promocionar los proyectos, aplicaciones e individuos que destaquen del ecosistema de NEAR, sobre todo aquellos que vienen de regiones de América Latina y España.
      </p>

      <p class="question">¿ Como puedo ponerme en contacto con NEAR Hispano?</p>
      <p class="answer">
        Por favor, llena el siguiente <a href="https://85cvz5vgyhm.typeform.com/to/Lu4IPM9O">formulario</a> 
        y un miembro del sindicato se pondrá en contacto contigo.
      </p>
    </template>

    <template v-slot:right-side >
      <img width="312" height="336" src="~/assets/images/faqs-illustration.svg" alt="Illustration faqs" class="img-fluid">
    </template>
  </base-section>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
.section-title {
  margin-bottom: 50px !important;
}

.question {
  color: #29c44d;
  font-size: 1.5rem;
  font-weight: bold;
}

.answer {
  text-align: justify;
}

.answer a {
  color: #29c44d;
}

</style>