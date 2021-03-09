<template>
  <div id="app">
    <HeaderNav/>
    <main class="main">
      <router-view/>
    </main>
    <FooterNav/>
  </div>
</template>

<script>
import HeaderNav from '@/components/HeaderNav.vue'
import FooterNav from '@/components/FooterNav.vue'

export default {
  name: 'App',
  components: {
    HeaderNav,
    FooterNav
  }
}
</script>

<style lang="scss">
@import 'assets/styles/style.scss';

#app {
  position: relative;
  height: 100vh;

  .main {
    margin-left: 7rem;
    margin-bottom: 5.5rem;
    padding: 2.2rem 1rem 0 1rem;
  }
}
</style>
