<template>
<div class="header-template">
  
  <header>
    <div class="header-80">
      <div class="header-left">
        <div class="logo">
          <img src="../assets/img/dc-logo.png" alt="">
        </div>
      </div>
    <div class="header-right">
      <ul>
        <li 
        :class="(link.status)? 'active' : 'null'"
        v-for="(link,index) in headerLinks" :key="index"
        @click='activateLink(index)'
        >
        
          <a href="#">{{link.text.toUpperCase()}}</a>
        </li>
        
      </ul>
    </div>
    </div>
  </header>
  <div class="head-jumbotron"></div>
</div>
  
</template>

<script>
export default {
  name:'Header',
  data(){
    return{
      headerLinks:[
        {
          text:'characters',
          status:true
        },
        {
          text:'comics',
          status:false
        },
        {
          text:'movies',
          status:false
        },
        {
          text:'tv',
          status:false
        },
        {
          text:'games',
          status:false
        },
        {
          text:'collectibles',
          status:false
        },
        {
          text:'videos',
          status:false
        },
        {
          text:'fans',
          status:false
        },
        {
          text:'news',
          status:false
        },
        {
          text:'shop',
          status:false
        },

      ]
    }
  },
  methods:{
    activateLink(index){
      this.headerLinks.forEach(link=>{
        link.status=false;
      });
      this.headerLinks[index].status=true;
    }
  }
}
</script>

<style lang='scss' scoped>
@import '../assets/css/headerStyle.scss';
.header-template .head-jumbotron{
  background: red;
  widows: 100%;
  height: 450px;
  background-image: url('../assets/img/jumbotron.jpg');
  background-size: cover;
}
</style>