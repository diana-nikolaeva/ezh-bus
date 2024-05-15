<template>
  <nav class="phone-menu-close">
    <div class="main-menu">
      <div class="logo">
        <img src="../assets/logo.png" alt="logo-ezh-bus">
      </div>
      <div class="phone-number">+7 (812) 500-65-65 </div>
      <button class="btn-open-phone-menu">
        <svg xmlns="http://www.w3.org/2000/svg" width="21" height="18" viewBox="0 0 21 18" fill="none">
          <rect width="21" height="2.47059" fill="#DE4C2F"/>
          <rect y="7.41211" width="21" height="2.47059" fill="#DE4C2F"/>
          <rect y="14.8232" width="21" height="2.47059" fill="#DE4C2F"/>
        </svg>
      </button>
    </div>
  </nav>
</template>

<style>
.phone-menu-close{
  padding: 12px;
  .main-menu{
    padding: 12px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0px 6px 40px 0px rgba(142, 24, 0, 0.50);
    height: 33px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    .logo{
      width: 54px;
      img{
        width: 100%;
      }
    }
    .phone-number{
      color:  #232323;
      text-align: center;
      font-family:  SVN-Gilroy,sans-serif;;
      font-size: 17px;
      font-style: normal;
      font-weight: 700;
      line-height: 160%; /* 27.2px */
    }
  .btn-open-phone-menu{
    border: 0;
  }
  }
}

</style>
<script setup lang="ts">

</script>