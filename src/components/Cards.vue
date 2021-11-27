<template>
<div class="cards">
  <div 
      v-if="cardList !== null"
      class="card" 
      style="width: 12rem;"
  >
      <div
          v-for="carta in cardList"
          :key="`carta${carta.author}`"
          class="card-body color-card">
        <img :src="carta.poster" class="card-img-top" alt="carta.author">
      </div>
      <div class="card color-card">
        <h3>{{ carta.title }}</h3>
        <div><span>{{ carta.author }}</span></div>
        <div><span>{{ carta.genre }}</span></div>
        <div><span>{{ carta.year }}</span></div>
      </div>
  </div>
  <div v-else>Loading</div>
</div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'Cards',
    data() {
      return {
        cardList: [],
      }
    },
    created() {
      this.getCards();
    },
    methods: {
      getCards() {
        axios
             .get('https://flynn.boolean.careers/exercises/api/array/music')
             .then(result =>{
               console.log(result.data);
               this.cardList = result.data
             })
             .catch(err => console.log(err));
      }
    }
}
</script>

<style lang='scss'>
    .color-card{
      background-color:  rgba(46, 58, 70, 1);
      h3{
        margin-bottom: 0;
      }
    }
    .card{
      text-align: center;
      color: white;
    }
</style>