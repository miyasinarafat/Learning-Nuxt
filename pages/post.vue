<template>
  <div class="container">
    <div>
      <h1 class="title">Lorem ipsum dolot</h1>
      <h3 class="subtitle">{{ name }}</h3>
      <br>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci debitis dolores ex id praesentium
        voluptatibus. Aliquid consequuntur cumque doloribus, eaque excepturi hic iste itaque iusto nemo odit perferendis
        similique totam?</p>
    </div>
  </div>
</template>

<script>
  export default {
    data({req}) {
      return {
        name: req ? 'Server' : 'Client'
      }
    }
  }
</script>
