<template>
  <div class="about">
    <h2 class="h2">{{ pageTitle }}</h2>
  </div>
</template>

<script>
export default {
  name: 'About',
  components: {

  },
  props: {
    pageTitle: {
      type: String,
      default: 'About'
    }
  }
}
</script>

<style scoped lang="scss">
.about {

}
</style>
