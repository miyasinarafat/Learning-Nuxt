<template>
  <div class="links">
    <nuxt-link :to="{ name: 'index' }" class="button--green">Home</nuxt-link>
    <nuxt-link to="/about" class="button--grey">About</nuxt-link>
    <nuxt-link to="/posts" class="button--grey">Blog</nuxt-link>
    <nuxt-link to="/contact" class="button--grey">Contact</nuxt-link>
  </div>
</template>

<script>
  export default {
    name: "Navbar"
  }
</script>

<style scoped>

</style>
