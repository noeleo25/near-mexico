
<template>
  <base-section 
    id="main-banner" 
    leftStyle="text-col d-flex flex-column justify-content-center"
    rightStyle="img-col d-none d-lg-block"
  >
    <template v-slot:left-side >
      <h1 
        class="typewrite" 
        data-period="2000" 
        data-type='[ "NEAR México" ]'
      >
        <span class="wrap"></span>
      </h1>
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
  mounted () {
    this.typeAnimation()
  },
  methods: {
    typeAnimation() {
      var elements = document.getElementsByClassName('typewrite')
      for (var i = 0; i < elements.length; i++) {
        var toRotate = elements[i].getAttribute('data-type')
        var period = elements[i].getAttribute('data-period')
        if (toRotate) {
          new txtType(elements[i], JSON.parse(toRotate), period)
        }
      }
      //CSS
      var css = document.createElement("style")
      css.innerHTML = ".typewrite > .wrap { border-right: 0.08em solid" + "" + "}"
      document.body.appendChild(css)
    }
  }
}
var txtType = function(el, toRotate, period) {
  this.toRotate = toRotate
  this.el = el
  this.loopNum = 0
  this.period = parseInt(period, 10) || 2000
  this.txt = ''
  this.tick()
  this.isDeleting = false
}

txtType.prototype.tick = function() {

  var i = this.loopNum % this.toRotate.length
  var fullTxt = this.toRotate[i]

  if (this.isDeleting) {
    this.txt = fullTxt.substring(0, this.txt.length - 1)
  } else {
    this.txt = fullTxt.substring(0, this.txt.length + 1)
  }

  this.el.innerHTML = '<span class="wrap">' + this.txt + '</span>'

  var that = this
  var delta = 200 - Math.random() * 100

  if (this.isDeleting) { 
    delta /= 2
  }

  if (!this.isDeleting && this.txt === fullTxt) {
    delta = this.period
    this.isDeleting = true
  } else if (this.isDeleting && this.txt === '') {
    this.isDeleting = false
    this.loopNum++
    delta = 500
  }

  setTimeout(() => { that.tick() }, delta)
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
  width: 120px;
  height: 42px;
  border: 0;
  border-radius: 6px;
  box-shadow: 0 3px 6px 0 rgba(0, 0, 0, 0.16);
  background-color: #29c44d;
  font-size: 1rem;
  color: #FFFFFF;
}
.join-btn::after {
  content: '';
  width: 5px; 
  height: 5px;
  border-radius: 100%;
  border: 6px solid #29c44d;
  position: absolute;
  z-index: -1;
  top: 63%;
  left: 13%;
  transform: translate(-50%, -50%);
  animation: ring 1.5s infinite;
}
@keyframes ring {
  0% {
    width: 30px;
    height: 30px;
    opacity: 1;
  }
  100% {
    width: 150px;
    height: 150px;
    opacity: 0;
  }
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