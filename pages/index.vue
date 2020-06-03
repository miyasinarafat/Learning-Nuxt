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
        <a
          href="/"
          class="button--green"
        >
          Home
        </a>
        <nuxt-link to="/post" class="button--grey">Post</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>
