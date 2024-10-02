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
        <picture>
          <source srcset="../assets/cars-main-banner.avif" type="image/avif">
          <img src="../assets/cars-main-banner.png" alt="">
        </picture>
      </figure>
    </div>
    <button class="btn btn-main-banner">
      <a href="#Калькулятор">Рассчитать стоимость</a>
    </button>
  </div>
</template>
<style scoped>
.desktop-main-banner{
  height: 577px;
  position: relative;
  @media screen and (min-width: 865px) {
    height: 1050px;
  }
}
.main-red-bcgr{
  width: 100%;
  height: 577px;
  position: absolute;
  top:0;
  @media screen and (min-width: 865px) {
    height: 1050px;
  }
  .first-layer{
    background: #DE4C2F;
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: 2;
  }
  .second-layer{
    width: 50%;
    position: absolute;
    z-index: 3;
    background:#721111;
    height: 100%;
    left: 50%;
    transform: translate(-50%);
    @media screen and (min-width: 865px) {
      width: 386px;
    }
  }
  .third-layer{
    max-width: 880px;
    width: 100%;
    height: 190px;
    background: #721111;
    clip-path: polygon(25% 0%, 75% 0%, 100% 100%, 0 100%);
    position: absolute;
    z-index: 4;
    bottom: 0;
    left: 50%;
    transform: translate(-50%);
    @media screen and (min-width: 865px) {
      width: 880px;
      height: 320px;
    }
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
  position: absolute;
  left: 46%;
  transform: translate(-50%);
  top:335px;
  z-index: 5;
  margin: 0;
  overflow: hidden;
  width: 80%;
  @media screen and (min-width: 360px){
    top:306px;
  }
  @media screen and (min-width: 500px){
    top:280px;
  }
  @media screen and (min-width: 600px){
    top:240px;
  }
  @media screen and (min-width: 865px){
    top:500px;
  }

  @media screen and (min-width: 1350px){
    top: 420px;
  }
  img{
    width: 100%;
    z-index: 5;
    position: relative;
    object-fit: cover;

  }
}
h1{
  color: #FFF;
  text-align: center;
  font-family: "Soyuz Grotesk", sans-serif;
  font-size: 49px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin-top: 20px;
  margin-bottom: 0;
  z-index: 5;
  position: relative;
  @media screen and (min-width: 865px){
    margin-top: 57px;
    font-size: 100px;
    margin-bottom: 11px;
  }
}
h4{
  color: #FFF;
  text-align: center;
  font-family: SVN-Gilroy, sans-serif;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 20px;
  z-index: 5;
  position: relative;
  margin-top: 10px;
  @media screen and (min-width: 865px){
    font-size: 30px;
  }
}
.btn-main-banner{
  position: absolute;
  bottom: 80px;
  left: 50%;
  transform: translateX(-50%);
  max-width: 427px;
  height: 50px;
  padding: 10px;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
  background: radial-gradient(99.74% 133.62% at 1.94% 0%, #FFF 0%, #E7E7E7 49.5%, #D2D2D2 100%);
  box-shadow: 0px 6px 0px 0px #9B9B9B, 0px 30px 40px 0px #590F00;
  font-family: "Soyuz Grotesk", sans-serif;
  font-size: 17px;
  z-index: 6;
  box-sizing: border-box;
  width:calc(100% - 40px);
  @media only screen and (min-width: 865px){
    width: 427px;
    height: 100px;
    font-size: 26px;
  }
  a{
    color: black;
    text-decoration: none;
  }
}
</style>
<script setup lang="ts">
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