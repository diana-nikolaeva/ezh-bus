<template>
    <div class="service black">
      <img :src="imgPath" alt="">
      <h3>{{title}}</h3>
      <a :href="link">Подробнее</a>
    </div>

</template>

<style scoped>
.container{
  max-width: 1250px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  margin: 0 auto;

  .service{
    height: 296px;
    position: relative;
    background:  #1B1C1E;
    margin-bottom: 20px;
    margin-right: 20px;
    flex-grow: 1;
    max-width: 400px;

    h3{
      color:  #FFF;
      font-family: "Soyuz Grotesk",sans-serif;
      font-size: 30px;
      font-style: normal;
      font-weight: 700;
      line-height: normal;
      width: 61%;
      margin-left: 40px;
      margin-top: 89px;
      z-index: 100;
    }
    a{
      color:  #DE4C2F;
      font-family: SVN-Gilroy,sans-serif;
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: normal;
      text-decoration-line: underline;
      margin-left: 53px;
    }
    img{
      width: 100%;
      position: absolute;
      bottom: 0;
    }
  }
  .service:last-child, .service:nth-child(3){
    margin-right: 0;

  }
  .service:first-child, .service:last-child{
    width: 506px;
    flex-grow: 0;
    max-width: 506px;
  }
  .service:nth-child(3), .service:nth-child(4){
    border-radius: 10px;
    border: 1px solid #535353;
    width: 298px;
    flex-grow: 0;
    background:linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
    a{
      color:#fff;
    }
  }
  .service.black{
    border-radius: 10px;
    border: 1px solid #535353;


  }

}


</style>
<script setup lang="ts">
defineProps(
  {
    imgPath: String,
    link: String,
    title:String
  }
);

</script>