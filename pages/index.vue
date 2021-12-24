<template>
  <div>
    <header>
      <MainNav/>
    </header>
    <main>
      <MainBanner />

      <CommunityNear/>

      <CommunityReasons/>

      <News/>

      <FrequentQuestions/>
    </main>
    <footer>
      
    </footer>
  </div>
</template>

<script>
import CommunityNear from '@/components/sections/CommunityNear.vue'
import CommunityReasons from '@/components/sections/CommunityReasons.vue'
import FrequentQuestions from '@/components/sections/FrequentQuestions.vue'
import MainBanner from '@/components/sections/MainBanner.vue'
import MainNav from '@/components/layouts/MainNav.vue'
import News from '@/components/sections/News.vue'

export default {
  components: {
    CommunityNear,
    CommunityReasons,
    FrequentQuestions,
    MainBanner,
    MainNav,
    News
  }
}
</script>

<style>
body {
  background-color: var(--secondary-color);
  color: var(--primary-color);
  font-size: 16px;
}

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
