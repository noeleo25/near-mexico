<template>
  <div>
    <header>
      <MainNav/>
    </header>
    <main>
      <MainBanner />
    </main>
    <footer>
      
    </footer>
  </div>
</template>

<script>
import MainNav from '@/components/layouts/MainNav.vue';
import MainBanner from '@/components/sections/MainBanner.vue';
export default {
  components: {
    MainBanner,
    MainNav
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
  padding: 40px 0;
}

@media (min-width: 768px) { 
  section {
    padding: 80px 0;
  }
}
</style>
