<template>
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
  <div v-else class="desktop-main-banner">
    <phone-menu-close></phone-menu-close>
    <h1>развозка сотрудников</h1>
    <h4>в Санкт-Петербурге и Ленинградской области</h4>
    <figure>
      <img src="../assets/cars-main-banner.png" alt="">
    </figure>
    <button class="btn btn-main-banner">Рассчитать стоимость</button>
  </div>
</template>

<style scoped>
.desktop-main-banner{
  background: url("../assets/bg-main-banner.png") center no-repeat;
  height: 1032px;
  position: relative;

}
figure{
  max-width: 1252px;
  width: 80%;
  margin: 0 auto;
  img{
    width: 100%;
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
  margin-top: 60px;
  margin-bottom: 11px;
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