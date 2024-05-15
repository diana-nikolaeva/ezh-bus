<script setup lang="ts">

const menuItems = [
  {titleMenuItem: 'Главная'},
  {titleMenuItem: 'Услуги'},
  {titleMenuItem: 'Калькулятор'},
  {titleMenuItem: 'Автопарк'},
  {titleMenuItem: 'О нас'},
  {titleMenuItem: 'Контакты'},
]

</script>

<template>
  <nav>
    <div class="header-phone-menu-open">
      <div class="logo">
        <img src="../assets/logo-mobile.png" alt="logo-ezh-bus">
      </div>
      <div class="menu-title">меню</div>
      <button class="close-btn">
        <img src="../assets/btn-close.png" alt="close">
      </button>
    </div>
    <ul class="main-menu-phone">
      <li class="menu-item selected" :key="item.titleMenuItem" v-for="item in menuItems" >
        <a href="/{{item.titleMenuItem}}">{{item.titleMenuItem}}</a>
      </li>
    </ul>
  </nav>

</template>

<style>
nav{
  display: flex;
  flex-direction: column;
  background: #DE4C2F;
  padding: 33px;
  .header-phone-menu-open{
    margin-bottom: 34px;
    position: relative;
    .logo{
      width: 54px;
      position: absolute;
      left: 0;
      img{
        width: 100%;
      }
    }
    .menu-title{
      color: #FFF;
      text-align: center;
      font-family: "Soyuz Grotesk",sans-serif;
      font-size: 30px;
      font-style: normal;
      font-weight: 700;
      line-height: normal;
    }
    .close-btn{
      width: 17px;
      height: 17px;
      background: #DE4C2F;
      border:0;
      cursor:pointer;
      position: absolute;
      right: 4px;
      top:10px;
      img{
        height: 100%;
      }
    }
  }
  .main-menu-phone{
    padding: 10px;
    margin-top: 0;
    .menu-item{
      list-style: none;
      text-align: center;
      margin-bottom: 30px;
      a{
        color:#fff;
        text-decoration: none;
        font-family: SVN-Gilroy,sans-serif;
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 1;
        padding: 5px 0;

      }

    }
    .menu-item.selected{
      a{
        border-bottom: #fff solid 5px;
      }
    }
  }
}

</style>


