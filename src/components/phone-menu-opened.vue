<script setup lang="ts">


import ListMenu from '@/components/list-menu.vue'

const emit = defineEmits(['closeMenu'])
function onClick() {
  emit('closeMenu');
}
</script>

<template>
  <nav>
    <div class="header-phone-menu-open">
      <div class="logo">
        <img src="../assets/logo-mobile.png" alt="logo-ezh-bus">
      </div>
      <div class="menu-title">меню</div>
      <button class="close-btn" @click="onClick">
        <img src="../assets/btn-close.png" alt="close">
      </button>
    </div>
    <list-menu></list-menu>
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
}

</style>


