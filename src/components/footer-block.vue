<script setup lang="ts">

</script>

<template>
  <section class="request-block">
    <div class="bcgr-red"></div>
    <div class="container-request-block">
      <div class="logo-footer-top">
        <img src="../assets/img.png" alt="">
      </div>
      <div class="rect-footer-right">
        <span>Мы скоро свяжемся с вами и всё расскажем!</span>
      </div>
      <h2>оставьте заявку</h2>
      <div class="descr">Заказывая автотранспортные услуги в нашей компании, вы получаете комфортную и надежную перевозку по оптимальной цене </div>
      <form action="">
        <input type="text" placeholder="Как Вас зовут?">
        <input placeholder="Ваш телефон или почта">
        <button type="submit" class="request-btn btn">оставить заявку</button>
      </form>
      <div class="person-data">Нажимая на кнопку "Отправить”, я соглашаюсь условиями обработки персональных данных</div>
      <div class="logo-footer">
        <img src="../assets/logo-footer.png" alt="">
      </div>
    </div>
  </section>
</template>

<style scoped>
  .container-request-block{
    background: linear-gradient(114deg, #3F3F3F 1.43%, #111 101.61%);
    padding: 0 20px;
    color: #fff;
    position: relative;
    @media only screen and (min-width: 865px){
      max-width: 1250px;
      margin: 0 auto;
      margin-top: -184px;
      border-radius: 10px;
    }
  }
  .logo-footer-top{
    display: none;
    @media only screen and (min-width: 865px){
      display: block;
      width: 210px;
      height: 225px;
      position: absolute;
      top:-10px;
      left: 40px;
    }
    img{
      width: 100%;
    }
  }
  .rect-footer-right{
    background: url("../assets/rect-white.png");
    background-size: cover;
    width: 200px;
    height: 210px;
    position: absolute;
    right: 40px;
   top:-10px;
    color: #DE4C2F;
    font-size: 20px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    font-family: "Soyuz Grotesk", sans-serif;
    span{
      width: 60%;
      display: block;
      margin: 40px 0 0 50px;
    }

  }
  .request-block {

    .bcgr-red{
      display: none;
      @media only screen and (min-width: 865px){
        display: block;
        background: #DE4C2F;
        height: 184px;
        width: 100%;
      }
    }
    h2 {
      padding-bottom: 20px;
      color: #fff;
      @media only screen and (min-width: 865px){
        font-size: 80px;
      }
    }

    .descr {
      text-align: center;
      font-size: 22px;
      width: 60%;
      margin: 0 auto;
    }

    form {
      margin-top: 25px;
      @media only screen and (min-width: 865px){
        display: flex;
        flex-direction: row;
        margin: 39px 172px 30px 172px;
        align-items: baseline;
      }
    }
    input{
      @media only screen and (min-width: 865px){
        width: 296px;
        margin-right: 22px;
      }
    }

    .request-btn {
      background: linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
      box-shadow: 0 6px 0 0 #6B1715, 0 30px 40px 0 #010101;
      color: #fff;
      margin-top: 7px;
      margin-bottom: 36px;
      padding: 10px 20px;
      @media only screen and (min-width: 865px){
        margin-top: 0;
        margin-bottom: 0;
      }
    }

    .person-data {
      color: #8C8C8C;
      text-align: center;
      font-family: 'SF Compact Display', sans-serif;
      font-size: 12px;
      font-style: normal;
      font-weight: 400;
      line-height: 130%;
      @media only screen and (min-width: 865px){
        padding-bottom: 66px;
      }
    }
    .logo-footer{
      width: 140px;
      height: 142px;
      margin: 0 auto;
      position: relative;
      @media only screen and (min-width: 865px){
        display: none;
      }
      img{
        width: 100%;
        position: absolute;
        bottom: 0;
      }
    }
  }

</style>