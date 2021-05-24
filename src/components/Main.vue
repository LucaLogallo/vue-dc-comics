<template>
  <main>
    <div class="main-container-80">
      <div class="cards-container">
        <!-- STAMPO N COMPONENTI COMICCARD -->
        <ComicCard
        v-for="(card,index) in cards"
        :key="index" 
        :thumb='card.thumb'
        :price='card.price'
        :series='card.series'
        :type='card.series'
        />
        <!-- nel tag comiccard che rappresenta la singola carta che gli ho passato e che ho creato in un componente passo con il bind i diversi attributi presi dal singolo oggetto carta presente nel documento js contenente l-array di oggetti aka carte -->
      </div>
      <button>LOAD MORE</button>
    </div>
  </main>
</template>



<script>

import ComicCard from '@/components/ComicCard' //passo la singola carta
import cards from '@/assets/data/dc-comics.js' //passo il file js contenente l'array di oggetti in modo tale da avere i diversi dati per ogni singola carta

export default {
  name:'Main',
  components:{
    ComicCard //passo la singola carta in modo da poterla inserire
  },
  data(){
    return{
      cards
    }
  }
}
</script>

<style lang='scss' scoped>
@import '../assets/css/main.scss';
@import '../assets/css/variables.scss';
button{
  padding: 5px 15px;
  border-radius: 0;
  outline: 0;
  border: none;
  margin-bottom: 30px;
  background-color: $lightbluecolor;
  color: white;
  font-weight: 500;
}
</style>