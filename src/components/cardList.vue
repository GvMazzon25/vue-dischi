<template>
 <div class="container">
    <div v-if="cardList !== null" class="row">
      <div
        v-for="card in cardList"
        :key="`card${card.year}`"
        class="col-6 col-md-4 col-lg-3"
      >
       
      </div>
   </div>
  <div v-else>Loading...</div>
 </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Cards',
    data() {
      return {
        cardList: null,
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
    
    .card-box{
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      .card-card{
        width: 200px;
        text-align: center;
        color: white;
        margin-right: 20px;
        background-color: rgba(46, 58, 70, 1);
        padding: 10px;
        margin-bottom: 20px;
         .img-box{
            width: 170px;
            height: 170px;
            margin: 20px auto;
          }
          div span{
            padding-bottom: 10px; 
          }
         .bg-color{
           margin: 0;
           background-color: rgba(46, 58, 70, 1);
        }
    }
    }
</style>