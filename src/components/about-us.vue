<script setup lang="ts">

</script>

<template>
  <a  name="О нас" href=""></a>
  <h2 class="about-us-title">о нас.</h2>
  <section class="about-us-block">
    <div class="banner">
      <picture>
        <source srcset="../assets/about-us-banner.avif" type="image/avif">
        <img src="../assets/about-us-banner.png" alt="about-ezh-bus-banner">
      </picture>
    </div>
    <div class="about-us">
      <h3>о нас.</h3>
      <span>Наша транспортная компания была основана в мае 2012 года в г. Санкт-Петербург высококвалифицированными специалистами, имеющими более семи лет опыта в сфере пассажирского транспорта, предоставления услуг по аренде автотранспорта с водителем</span>
      <h4> Что полезно знать о нашей транспортной компании?</h4>
      <span>Профильным направлением компании является организация и ведение услуг служебной развозки сотрудников (персонала). Мы организуем и оказываем услуги на территории г. Санкт-Петербурга и Ленинградской области самого высокого качества.<br/> Если вы желаете получить качественные, надежные, безопасные, своевременные и современные транспортные услуги, будьте уверены, что выбрав нашу компанию, вы сделаете не только правильный выбор, но и сократите расходы, так как компания имеет огромный багаж знаний и инструментов для сохранения идеального баланса «Цены и Качества»</span>
    </div>
  </section>


</template>

<style scoped>
.about-us-title{
  padding-bottom: 17px;
  @media screen and (min-width: 865px){
    display: none;
  }
}
 .about-us-block{
   display: flex;
   flex-direction: column;
   @media screen and (min-width: 865px){
     flex-direction: row-reverse;
   }
   h3{
     display: none;
     @media screen and (min-width: 865px){
       display: block;
       color:  #232323;
       text-align: center;
       font-family: "Soyuz Grotesk",sans-serif;
       font-size: 45px;
       font-style: normal;
       font-weight: 700;
       line-height: normal;
       margin:0;
       padding-top: 27px;
     }
   }
   .banner{
     background: #721111;
     padding-top: 30px;
     @media screen and (min-width: 865px){
       position: relative;
       width: 825px;
     }
     img{
       width: 100%;
       max-height: 80%;
       @media screen and (min-width: 865px){
         width: auto;
         max-width: 100%;
         position: absolute;
         left: -110px;
         top:50px;

       }
     }
   }
   .about-us{
     padding: 27px 20px;
     @media screen and (min-width: 865px){
       width: 576px;
       margin-right: 130px;
     }
     h4{
       color:  #232323;
       font-family: "Soyuz Grotesk",sans-serif;
       font-size: 22px;
       font-style: normal;
       font-weight: 700;
       line-height: 100%;
     }
   }
 }
</style>