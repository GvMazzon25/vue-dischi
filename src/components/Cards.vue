<template>
 <div class="card-box">
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
    <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
    <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
   <div class="card-card">
     <div class="img-box">
       <img src="" alt="">
     </div>
     <div class="bg-color"><h3 class="bg-color">Title</h3></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
     <div class="bg-color"><span class="bg-color">test</span></div>
   </div>
 </div>
</template>

<script>
import axios from 'axios';

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