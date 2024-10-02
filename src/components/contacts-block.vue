<script setup lang="ts">

</script>

<template>
  <section class="contact-block">
    <a  name="Контакты" href=""></a>
    <h2>контакты.</h2>
    <div class="container-contact-block">
      <div class="maps">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2003.87653558808!2d30.47602017738414!3d59.85119056913918!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46962f6989903c1b%3A0x349637947f612035!2z0JHQpiAi0J7QsdGD0YXQvtCy0Yot0KbQtdC90YLRgCI!5e0!3m2!1sru!2sru!4v1727857291817!5m2!1sru!2sru"></iframe>
      </div>
      <div>
        <div class="order-call">
          <img src="../assets/phone-icon.png" alt="phone-ezh-bus" class="img-phone">
          <div class="container-contacts">
            <a href="tel:+79052163007" class="phone">+7 (905) 216-30-07 </a>
            <div class="call-back">
              <a href="/">Закакзать обратный звонок</a>
            </div>
          </div>
        </div>
        <div class="address-container">
          <img src="../assets/navigate-icon.png" alt="" class="navigate-icon-ezh-bus">
          <div class="address">Санкт-Петербург, Обуховской обороны д. 271,<br/> БЦ "Обуховъ-Центр"</div>
        </div>
        <a href="" class="privacy"> Политика конфиденциальности</a>
      </div>
    </div>
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
   .container-contact-block{
     display: flex;
     flex-direction: column;
     max-width: 300px;
     margin: 0 auto;
     @media only screen and (min-width: 865px) {
       flex-direction: row-reverse;
       max-width: 1250px;
     }
   }
   .maps{
    margin-bottom: 50px;
     width: 280px;
     height: 260px;
     @media only screen and (min-width: 865px){
       width: 616px;
       height: 517px;
       margin-left: 200px;
       border-radius: 10px;
     }
   }
   iframe{
     width: 100%;
     height: 100%;
   }
   .order-call{
     display: flex;
     flex-direction: row;
     @media only screen and (min-width: 865px){
       margin-top: 71px;
     }
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