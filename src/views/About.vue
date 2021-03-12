<template>
  <div class="about">
    <h1 class="h1">{{ pageTitle }}</h1>

    <div class="content">

    </div>
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

<style lang="scss" scoped>

</style>
