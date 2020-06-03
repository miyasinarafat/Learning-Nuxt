<template>
  <div class="container">
    <div>
       <div v-for="post in posts">
        <h1 class="subtitle"><a :href="`posts/${post.slug}`">{{ post.title }}</a></h1>
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
        posts: [
          {
            slug: 'balut',
            title: 'What is Balut?',
            content: 'If someone placed balut on your plate, you might think they were serving you a hardboiled egg. That is, until you cracked it open and a fully intact duck embryo spilled out. Balut, considered a delicacy in many Asian countries, is produced when fertilized duck eggs are placed in warm sunlight. After about eight days, the eggs are held up to the light and checked to ensure that the budding embryo is ready. Then, the eggs are cooked and served with a dash of salt and a few squirts of lemon juice.'
          },
          {
            slug: 'whereIsIt',
            title: 'Where is the sign in button??',
            content: 'I\'ve stalked the forum for a while, reading everything closely, but today I decided that it was time to register as a user. So I did, this morning! But now, when I came back to the forum, I cannot seem to find the damn sign in button? WHERE IS IT???!??'
          },
          {
            slug: 'how',
            title: 'How can I fix this problem?',
            content: 'Please help me. I dont know what is the best way to fix my problem. I cant reproduce and I cant tell more info. Can someone help me asap??? I am in a hurry!!!'
          }
        ]
      }
    },
    computed: {
      post() {
        return this.posts.find(post => post.slug == this.slug)
      }
    }
  }
</script>
