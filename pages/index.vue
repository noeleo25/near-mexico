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

@media (min-width: 768px) { 
  section {
    padding-top: 80px;
  }
}
</style>
