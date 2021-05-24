<template>
  <div class="single-card">
    <div class="img-container">
      <img :src="this.thumb" alt="">
    </div>
    <div class="text-container">
      <h4>{{this.series.toUpperCase()}}</h4>
    </div>
    
  </div>
</template>

<script>
export default {
  name:"ComicCard",
  props:{ //con il props dichiaro le variabili che riceverò dal documento "padre" con il nome : tipo
    thumb: String,
    price: String,
    series: String,
    type: String
  }
}
</script>

<style lang="scss">
  .single-card{
    flex-basis: calc(100% / 6);
    height: 100%;
    padding: 10px;
    .img-container{
      max-height: 230px;
      overflow: hidden;
      /* background: red; */
      img{
        width: 233px;
        cursor: pointer;
        
      }
    }
    .text-container{
      /* background: red; */
      /* height: 20px; */
      width:100%;
      h4{
      margin-top: 10px;
      /* width: 100%; */
    }
    }
    
    
  }
</style>