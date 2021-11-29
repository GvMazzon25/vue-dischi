<template>
  <div classe="card">
       <img :src="card.image" alt="">
        <h3>{{card.poster}}</h3>
        <div>{{card.author}}</div>
        <div>{{card.year}}</div>
        <div>{{card.genre}}</div>
  </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        poster: String,
        author: String,
        year: String,
        card: String,
    }
}
</script>

<style>

</style>