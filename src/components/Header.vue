<template>
  <div class="wrap">
    <div class="box80">
    <div class="logo">
      <img src="@/assets/img/dc-logo.png" alt="">
    </div>
    <div class="menu">
      <ul>
        <li
        v-for="(link ,index) in links" :key="index">
        <a >{{link.nome}}</a>
        <div class="quadrato"></div>
        </li>
      </ul>
    </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return{
    links:[

      {
        nome: 'characters',
        url:'/',
        flag: false      
      },
      {
        nome: 'comics',
        url:'/',
        flag: false      
      },
      {
        nome: 'movies',
        url:'/',
        flag: false      
      },
      {
        nome: 'tv',
        url:'/',
        flag: false      
      },
      {
        nome: 'games',
        url:'/',
        flag: false      
      },
      {
        nome: 'collectibles',
        url:'/',
        flag: false      
      },
      {
        nome: 'videos',
        url:'/',
        flag: false      
      },
      {
        nome: 'fans',
        url:'/',
        flag: false      
      },
      {
        nome: 'news',
        url:'/',
        flag: false      
      },
      {
        nome: 'shop',
        url:'/',
        flag: false      
      }
    ] 
    }

  }
}
</script> 

<style lang='scss' scoped>
@import '@/assets/style/general.scss';

.wrap{
  height: 120px;
  /* background-color: red; */

  .box80{
  width: $box80; //$box80
  height: 100%;
  margin: auto;
  padding: 10px;
  display: flex;
  align-items: center;

  .logo{
    width: 40%;
    img{
      height: 80px;
  }
  }
  .menu{
    width: 70%;
    height: 100%;
    display: flex;
    align-items: center;

    ul{
      list-style: none;

      li{
        display: inline-block;
        margin: 10px;
        font-size: 11px;
        text-transform: uppercase;
        height: 120px;
        line-height: 120px;
        position: relative;
        cursor: pointer;
        transition: background 0.4s;
        color: $colorTextGrey;
        &:hover,
        &.active{
        color: $colorTextBlue;
        }
        .quadrato{
          display: none;
          position: absolute;
          bottom: 0;
          height: 5px;
          width: 100%;
          background-color: $colorTextBlue;
        }
        &:hover .quadrato{
          display: block;
        }
      }
    }
  }
}
}
</style>