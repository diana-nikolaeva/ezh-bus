<script setup lang="ts">

</script>

<template>
  <section class="contact-block">
    <h2>контакты.</h2>
    <div class="maps">
      <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3Ae90c77c578d6659d60a671c2a0c3cfeeb46cebe2afac01b781ed3ad6a02595d3&amp;source=constructor" width="280" height="260" frameborder="0"></iframe>
    </div>
    <div class="order-call">
      <img src="../assets/phone-icon.png" alt="phone-ezh-bus" class="img-phone">
      <div class="container-contacts">
        <div class="phone">+7 (812) 500-65-65</div>
        <div class="call-back">
          <a href="/">Закакзать обратный звонок</a>
        </div>
      </div>
    </div>
    <div class="address-container">
      <img src="../assets/navigate-icon.png" alt="" class="navigate-icon-ezh-bus">
      <div class="address">Санкт-Петербург, Новороссийская 26/2 офис 108</div>
    </div>
    <a href="" class="privacy"> Политика конфиденциальности</a>
  </section>
</template>

<style scoped>
 .contact-block{
   background: #DE4C2F;
   padding: 0 20px 21px 20px;
   color:#fff;
   h2{
     color:#fff;
     padding-bottom: 31px;
   }
   a{
     color: #fff;
     font-family: SVN-Gilroy,sans-serif;
     font-size: 16px;
     font-style: normal;
     font-weight: 400;
     line-height: 130%;
     text-decoration-line: underline;
   }
   .maps{
    margin-bottom: 50px;
   }
   .order-call{
     display: flex;
     flex-direction: row;
     .container-contacts{
       display: flex;
       flex-direction: column;
       margin-bottom: 50px;
     }
     img{
       width: 20px;
       height: 20px;
       margin-right: 10px;
     }
   }
   .address-container{
     display: flex;
     flex-direction: row;
     margin-bottom: 50px;
     img{
       width: 20px;
       height: 24px;
       margin-right: 10px;
     }
   }
   .privacy{
     margin-left: 32px;
   }
 }
</style>