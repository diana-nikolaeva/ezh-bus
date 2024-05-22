<template>
    <phone-menu-opened
      v-if="menuIsOpened"
      @closeMenu="menuPhoneClose"
    ></phone-menu-opened>
    <phone-menu-close
      v-if ="!menuIsOpened"
      @openMenu="onOpenMenu"
    ></phone-menu-close>
</template>

<style>
@media (min-width: 1024px) {

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
</script>