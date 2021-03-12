<template>
  <article :class="className">
    <h3>{{ title }}</h3>
    <p>{{ content }}</p>
    <img :src="require(`../../public/medias/projects/${img}`)" :alt="alt">
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
h1{
  font-weight: 500;
}
</style>
