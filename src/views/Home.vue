<template>
  <div class="home">
    <h1 class="h1">{{ pageTitle }}</h1>

    <p class="about-me">
      Hello,<br>
      je m'appelle Thomas je suis développeur & intégrateur web au sein d'une <a class="link" target="_blank" rel="noopener noreferrer" href="">agence exotique</a> sur <a class="link" target="_blank" rel="noopener noreferrer" href="https://goo.gl/maps/iE4Jme1qKVDypAK78">Strasbourg</a> !
    </p>

    <div class="content">
      <CardProject
        className="hey"
        title="Hello Hello"
        content="ceci est mon content"
        img="css3.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="docker.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="git.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="html5.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="js.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="php.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="sass.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="symfony.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="vuejs.svg" alt="Mon logo"
      />

      <CardProject
        className="ho"
        title="Bye Bye"
        content="Contenu de card project"
        img="wordpress.svg" alt="Mon logo"
      />
    </div><!-- .content -->
  </div><!-- .home -->
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

<style lang="scss" scoped>

</style>
