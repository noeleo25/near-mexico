<template>
  <div>
    <header>
      <MainNav/>
    </header>
    <main>
      <Banner />

      <CommunityNear/>

      <CommunityReasons/>

      <News/>

      <FrequentQuestions/>
    </main>
    <MainFooter/>
  </div>
</template>

<script>
import Banner from '@/components/sections/Banner.vue'
import CommunityNear from '@/components/sections/CommunityNear.vue'
import CommunityReasons from '@/components/sections/CommunityReasons.vue'
import FrequentQuestions from '@/components/sections/FrequentQuestions.vue'
import MainFooter from '@/components/layouts/MainFooter.vue'
import MainNav from '@/components/layouts/MainNav.vue'
import News from '@/components/sections/News.vue'

export default {
  components: {
    Banner,
    CommunityNear,
    CommunityReasons,
    FrequentQuestions,
    MainFooter,
    MainNav,
    News
  },
  head() {
    return {
      title: 'NEAR México'
    }
  }
}
</script>

<style>
section {
  padding-top: 40px;
}

.section-title {
  font-size: 2rem;
  font-weight: 800;
  text-transform: uppercase;
  margin-bottom: 20px !important;
}

/* Styles to CommunityReasons and FrequentQuestions sections */

#community-reasons .section-title,
#frequent-questions .section-title {
  margin-bottom: 50px !important;
  animation: moveToBottom 1s ease;
}

.question-container .question {
  color: #29c44d;
  font-size: 1.5rem;
  font-weight: bold;
}

.question-container .answer {
  text-align: justify;
}

.question-container:nth-child(1) {
  animation: moveToTop 1s ease;
}

.question-container:nth-child(2) {
  animation: moveToTop 1.5s ease;
}

.question-container:nth-child(3) {
  animation: moveToTop 2s ease;
}

.right-col img {
  animation: slideToLeft 1.5s ease;
}

/* Animations */
@keyframes moveToBottom {
  0% {
    opacity: 0;
    transform: translate(0, -100px);
  }
  25% {
    opacity: .5;
  }
  100% {
    transform: translate( 0, 0);
  }
}

@keyframes moveToTop {
  0% {
    opacity: 0;
    transform: translate(0, 50px);
  }
  25% {
    opacity: .5;
  }
  100% {
    transform: translate( 0, 0);
  }
}

@keyframes slideToLeft {
  0% {
    opacity: 0;
    transform: translate(100px, 0) scale(0.5);
  }
  50% {
    transform: scale(1);
  }
  100% {
    transform: translate( 0, 0);
  }
}

@media (min-width: 768px) { 
  section {
    padding-top: 80px;
  }
}
</style>
