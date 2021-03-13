<template>
  <article :class="className">
    <h3>{{ title }}</h3>
    <p>{{ content }}</p>
    <img :src="require(`../../public/medias/stack/${img}`)" :alt="alt">
  </article>
</template>

<script>
export default {
  name: 'CardProject',
  props: {
    className: String,
    title: String,
    content: String,
    img: String,
    alt: String
  }
}
</script>

<style lang="scss" scoped>

</style>
