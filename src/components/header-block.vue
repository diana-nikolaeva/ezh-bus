<template>
  <div class="desktop-main-banner">
    <template v-if="isPhone">
      <phone-menu-opened
        v-if="menuIsOpened"
        @closeMenu="menuPhoneClose"
      ></phone-menu-opened>
      <phone-menu-close
        v-if ="!menuIsOpened"
        @openMenu="onOpenMenu"
      ></phone-menu-close>
    </template>
    <template v-else>
      <phone-menu-close></phone-menu-close>
    </template>
    <h1>развозка сотрудников</h1>
    <h4>в Санкт-Петербурге и Ленинградской области</h4>
    <div class="main-red-bcgr">
      <div class="first-layer"></div>
      <div class="second-layer"></div>
      <div class="third-layer"></div>
      <div class="fourth-layer"></div>
      <figure>
        <img src="../assets/cars-main-banner.png" alt="">
      </figure>
    </div>
    <button class="btn btn-main-banner">Рассчитать стоимость</button>
  </div>
</template>
<style scoped>
.desktop-main-banner{
  height: 1032px;
  position: relative;
}
.main-red-bcgr{
  width: 100%;
  height: 1032px;
  position: absolute;
  top:0;
  .first-layer{
    background: #DE4C2F;
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: 1;
  }
  .second-layer{
    width: 386px;
    position: absolute;
    z-index: 2;
    background:#721111;
    height: 100%;
    left: 50%;
    transform: translate(-50%);
  }
  .third-layer{
    width: 880px;
    height: 320px;
    background: #721111;
    clip-path: polygon(25% 0%, 75% 0%, 100% 100%, 0 100%);
    position: absolute;
    z-index: 3;
    bottom: 0;
    left: 50%;
    transform: translate(-50%);
  }
  .fourth-layer{
    background-image: radial-gradient(circle, #e16759, #DE4C2F);
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: 1;
    left: 50%;
    top:0;
    transform: translate(-50%);
  }
}
figure{
  max-width: 1252px;
  width: 70%;
  position: absolute;
  left: 46%;
  transform: translate(-50%);
  top:500px;
  z-index: 4;
  margin: 0;
  @media screen and (min-width: 1080px){
    top: 500px;
  }
  @media screen and (min-width: 1350px){
    top: 420px;
  }
  img{
    width: 100%;
    z-index: 4;
    position: relative;

  }
}
h1{
  color: #FFF;
  text-align: center;
  font-family: "Soyuz Grotesk", sans-serif;
  font-size: 100px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin-top: 30px;
  margin-bottom: 11px;
  z-index: 5;
  position: relative;
  @media screen and (min-width: 1080px){
    margin-top: 60px;
  }
}
h4{
  color: #FFF;
  text-align: center;
  font-family: SVN-Gilroy, sans-serif;
  font-size: 30px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 20px;
  z-index: 5;
  position: relative;
  margin-top: 10px;
}
.btn-main-banner{
  position: absolute;
  bottom: 80px;
  left: 50%;
  transform: translateX(-50%);
  width: 427px;
  max-width: 427px;
  height: 100px;
  padding: 10px;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
  background: radial-gradient(99.74% 133.62% at 1.94% 0%, #FFF 0%, #E7E7E7 49.5%, #D2D2D2 100%);
  box-shadow: 0px 6px 0px 0px #9B9B9B, 0px 30px 40px 0px #590F00;
  font-family: "Soyuz Grotesk", sans-serif;
  font-size: 26px;
  z-index: 5;
}
</style>
<script setup>
import { ref } from 'vue';
let menuIsOpened = ref(false);

function onOpenMenu(){
  menuIsOpened.value = true;
}
function menuPhoneClose(){
  menuIsOpened.value = false;
}

import PhoneMenuClose from '@/components/phone-menu-close.vue'
import PhoneMenuOpened from '@/components/phone-menu-opened.vue'
defineProps({ isPhone: Boolean });
</script>