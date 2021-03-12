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
    padding: 1rem 1rem 0 1rem;
  }

  .highlight {
    font-weight: 500;
    background-image: linear-gradient(var(--hover), var(--hover));
    background-repeat: no-repeat;
    background-position: left bottom;
    background-size: 100% 1rem;
  }

  // Link effect & hover
  .link {
    font-weight: 500;
    text-decoration: none;
    color: inherit;
    animation: out .2s ease;

    @keyframes out {
      from {
        background-image: linear-gradient(var(--hover), var(--hover));
        background-repeat: no-repeat;
        background-position: right bottom;
        background-size: 100% 0.8rem;
      }
      to {
        background-image: linear-gradient(var(--hover), var(--hover));
        background-repeat: no-repeat;
        background-position: right bottom;
        background-size: 0% 0.8rem;
      }
    }

    &:hover {
      background-image: linear-gradient(var(--hover), var(--hover));
      background-repeat: no-repeat;
      background-position: left bottom;
      background-size: 100% 0.8rem;
      animation: in .2s ease;

      @keyframes in {
        from {
          background-image: linear-gradient(var(--hover), var(--hover));
          background-repeat: no-repeat;
          background-position: left bottom;
          background-size: 0% 0.8rem;
        }
        to {
          background-image: linear-gradient(var(--hover), var(--hover));
          background-repeat: no-repeat;
          background-position: left bottom;
          background-size: 100% 0.8rem;
        }
      }
    }
  }
}
</style>
