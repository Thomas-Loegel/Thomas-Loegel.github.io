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

  .main {
    padding: 1rem 0 0 8rem;

    &::before {
      content: "";
      position: absolute;
      top: 0;
      right: 0;
      bottom: 4.4rem;
      left: 7rem;
      background-image:
      linear-gradient(var(--white), var(--white));
      background-repeat: no-repeat;
      background-position: left;
      background-size: .05rem 100%;
    }
  }
}
</style>
