<template>
  <nav class="phone-menu-close">
    <div class="main-menu">
      <div class="logo">
        <img src="../assets/logo.png" alt="logo-ezh-bus" />
      </div>
      <list-menu class="list-menu-desktop"></list-menu>
      <a href="tel:+79052163007" class="phone-number">+7 (905) 216-30-07 </a>
      <button class="btn-open-phone-menu" @click="onClick">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="21"
          height="18"
          viewBox="0 0 21 18"
          fill="none"
        >
          <rect width="21" height="2.47059" fill="#DE4C2F" />
          <rect y="7.41211" width="21" height="2.47059" fill="#DE4C2F" />
          <rect y="14.8232" width="21" height="2.47059" fill="#DE4C2F" />
        </svg>
      </button>
    </div>
  </nav>
</template>

<style scoped>
.phone-menu-close {
  padding: 12px;
  z-index: 10;
  position: relative;
  background: none;
  @media screen and (min-width: 865px) {
    padding-top: 30px;
  }
  .main-menu {
    padding: 12px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0px 6px 40px 0px rgba(142, 24, 0, 0.5);
    height: 57px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 1250px;
    box-sizing: border-box;
    @media only screen and (min-width: 865px) {
      height: 117px;
      margin: 0 auto;
    }
    @media only screen and (max-width: 1250px) {
      width: 100%;
    }
    .logo {
      width: 54px;
      @media only screen and (min-width: 865px) {
        width: 146px;
        height: 84px;
      }
      img {
        width: 100%;
      }
    }
    .phone-number {
      color: #232323;
      text-align: center;
      font-family: SVN-Gilroy, sans-serif;
      font-size: 17px;
      font-style: normal;
      font-weight: 700;
      line-height: 160%;
      text-decoration: none;
    }
    .btn-open-phone-menu {
      border: 0;
      background: transparent;
      @media only screen and (min-width: 865px) {
        display: none;
      }
    }
    .list-menu-desktop {
      display: none;
      @media only screen and (min-width: 865px) {
        display: flex;
      }
    }
  }
}
</style>
<script setup lang="ts">
import ListMenu from '@/components/list-menu.vue'

const emit = defineEmits(['openMenu'])
function onClick() {
  emit('openMenu')
}
</script>
