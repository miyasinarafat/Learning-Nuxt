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
    head() {
      return {
        title: this.post.title,
        meta: [
          { name: 'twitter:title', content: this.post.title},
          { name: 'twitter:description', content: this.post.content},
          { name: 'twitter:image', content: 'https://i.imgur.com/UYP2umJ.png'},
          { name: 'twitter:card', content: 'summary_large_image'}
        ]
      };
    },
    computed: {
      post() {
        return this.$store.state.posts.all.find(post => post.slug == this.slug)
      }
    }
  }
</script>
