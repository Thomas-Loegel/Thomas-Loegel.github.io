<template>
  <div class="home">
    <h1>{{ pageTitle }}</h1>

    <CardProject
      className="hey"
      title="Hello Hello"
      content="ceci est mon content"
      img="logo.png" alt="Mon logo"
    />

    <CardProject
      className="ho"
      title="Bye Bye"
      content="Contenu de card project"
      img="logo.png" alt="Mon logo"
    />
    <CardProject
      className="ho"
      title="Bye Bye"
      content="Contenu de card project"
      img="logo.png" alt="Mon logo"
    />
    <CardProject
      className="ho"
      title="Bye Bye"
      content="Contenu de card project"
      img="logo.png" alt="Mon logo"
    />
    <CardProject
      className="ho"
      title="Bye Bye"
      content="Contenu de card project"
      img="logo.png" alt="Mon logo"
    />
    <CardProject
      className="ho"
      title="Bye Bye"
      content="Contenu de card project"
      img="logo.png" alt="Mon logo"
    />
    <CardProject
      className="ho"
      title="Bye Bye"
      content="Contenu de card project"
      img="logo.png" alt="Mon logo"
    />
  </div>
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
