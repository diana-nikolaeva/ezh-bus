<script setup>
const btnUp = document.querySelector('go-back-btn');
// window.addEventListener('scroll',function(){
//   if (window.scrollY >  document.documentElement.clientHeight){
//     btnUp.classList.add('visible')
//   }
// })
</script>
<template>
  <div class="go-back-btn">
    <a href="#Услуги"></a>
  </div>
</template>
<style scoped>
  .go-back-btn{
    width: 30px;
    height: 30px;
    border-top: 10px solid #1B1C1E;
    border-right: 10px solid #1B1C1E;
    margin-right: 60px;
    transform: rotate(-45deg);
    position: fixed;
    bottom: 40px;
    right: 40px;
    z-index: 15;
    display: none;
    &.visible{
      display: block;
    }
  }
  a{
    width: 30px;
    height: 30px;
    display: block;
  }
</style>
