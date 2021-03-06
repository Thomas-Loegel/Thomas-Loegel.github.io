<template>
  <main>
    <h1>{{ pageTitle }}</h1>

    <CardProject
      className="hey"
      title="Welcome to Your Vue.js App"
      content="ceci est mon content"
      img="logo.png" alt="Mon logo"
    />
  </main>
</template>

<script>
// @ is an alias to /src
import CardProject from '@/components/CardProject.vue'

export default {
  name: 'Home',
  components: {
    CardProject
  },
  props: {
    pageTitle: {
      type: String,
      default: 'Home Page'
    }
  }
}
</script>
