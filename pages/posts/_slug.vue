<template>
  <div class="container">
    <div>
      <h1 class="title">{{ post.title }}</h1>
      <br>
      <p>{{ post.content }}</p>
    </div>
  </div>
</template>

<script>
  export default {

    data() {
      return {
        slug: this.$route.params.slug,
      }
    },
    computed: {
      post() {
        return this.$store.state.posts.all.find(post => post.slug == this.slug)
      }
    }
  }
</script>
