<template>
  <div class="container">
    <div>
       <div v-for="post in posts">
        <h1 class="subtitle">
          <nuxt-link :to="{name: 'posts-slug', params: {slug: post.slug}}">{{ post.title }}</nuxt-link>
        </h1>
        <br>
        <p>{{ post.content }}</p>
      </div>
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
        title: 'Posts page',
        meta: [
          { name: 'twitter:title',  content: 'Posts page'},
          { name: 'twitter:description', content:  'Nuxt + Vue School = 🍕'},
          { name: 'twitter:image', content: 'https://i.imgur.com/UYP2umJ.png'},
          { name: 'twitter:card', content: 'summary_large_image'}
        ]
      };
    },
    computed: {
      post() {
        return this.posts.find(post => post.slug == this.slug)
      },

      posts() {
        return this.$store.state.posts.all;
      }
    }
  }
</script>
