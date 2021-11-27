<template>
  <div class="card" style="width: 12rem;">
      <div class="card-body color-card">
        <img src="" class="card-img-top" alt="...">
      </div>
      <div class="card color-card">
        <h3>Title</h3>
        <div><span>Autore</span></div>
        <div><span>Data</span></div>
        <div><span>Genere</span></div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Cards',
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