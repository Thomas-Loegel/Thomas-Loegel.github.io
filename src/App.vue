<template>
  <div id="app">
    <HeaderNav/>
    <router-view/>
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
</style>
