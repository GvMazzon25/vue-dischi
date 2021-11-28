<template>
  <main>
      <div class="card-container">
          <Cards />
      </div>
  </main>
</template>

<script>
import Cards from './Cards.vue'

export default {
    name: 'Main',
    components: {
      Cards,
      
  }
}
</script>

<style lang='scss'>
   @import '@/style/Main.scss';
</style>