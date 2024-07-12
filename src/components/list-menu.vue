<script setup lang="ts">
const menuItems = [
  {
    titleMenuItem: 'Главная',
    linkMenuItem:'#Главная'
  },
  {
    titleMenuItem: 'Услуги',
    linkMenuItem:'#Услуги'
  },
  {
    titleMenuItem: 'Калькулятор',
    linkMenuItem:'#Калькулятор'
  },
  {
    titleMenuItem: 'Автопарк',
    linkMenuItem:'#Автопарк'
  },
  {
    titleMenuItem: 'О нас',
    linkMenuItem:'#О нас'
  },
  {
    titleMenuItem: 'Контакты',
    linkMenuItem:'#Контакты'
  },
]
</script>

<template>
  <ul class="main-menu-phone">
    <li class="menu-item selected" :key="item.titleMenuItem" v-for="item in menuItems" >
      <a :href="item.linkMenuItem">{{item.titleMenuItem}}</a>
    </li>
  </ul>
</template>

<style scoped>
.main-menu-phone{
  padding: 10px;
  margin-top: 0;
  @media only screen and (min-width: 865px){
    display: flex;
    flex-direction: row;
    margin-bottom: 0;
  }
  .menu-item{
    list-style: none;
    text-align: center;
    margin-bottom: 30px;
    @media only screen and (min-width: 865px){
      margin-bottom: 0;
      margin-right:30px;
    }
  }
  a{
    color:#fff;
    text-decoration: none;
    font-family: SVN-Gilroy,sans-serif;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 1;
    padding: 5px 0;
    @media only screen and (min-width: 865px){
      color:  #232323;
      text-align: center;
    }
  }

  .menu-item.selected{
    a{
      border-bottom: #fff solid 5px;
    }
  }
}
</style>