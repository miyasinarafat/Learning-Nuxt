<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        learning-nuxt
      </h1>
      <h2 class="subtitle">
        My beautiful Nuxt.js project
      </h2>
      <div class="links">
        <nuxt-link to="/" class="button--green">Home</nuxt-link>
        <nuxt-link to="/posts" class="button--grey">Posts</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  head() {
    return {
      title: 'Home Page  🍕',
      meta: [
        { name: 'twitter:title', content: 'Nuxt Fundamentals by Vue School'},
        { name: 'twitter:description', content: 'Nuxt + Vue School = 🍕'},
        { name: 'twitter:image', content: 'https://i.imgur.com/UYP2umJ.png'},
        { name: 'twitter:card', content: 'summary_large_image'}
      ]
    }
  }
}
</script>
