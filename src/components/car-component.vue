<script setup lang="ts">
defineProps(
  {
    imgPath: String,
    title:String,
    price:String,
    descr:String,
    seats:String
  }
);
</script>

<template>
  <div>
    <div class="img-car">
      <img :src="imgPath" alt="">
    </div>
    <div class="title-car">{{title}}</div>
    <div class="price-car">{{price}} ₽/час</div>
    <div class="descr-car">
      <span>{{descr}}</span>
      <span class="more-details">
        <a href="/">Подробнее</a>
      </span>
    </div>
    <div class="order-block">
      <div class="wrapper-number-seats">
        <div class="img-people">
          <img src="../assets/order-people.png" alt="">
        </div>
        <div class="number-seats">{{seats}}</div>
      </div>
      <button class="order-car-btn">заказать</button>
    </div>
  </div>

</template>

<style scoped>
    .img-car{
      img{
        width: 100%;
      }
    }
    .title-car{
      color:  #232323;
      font-family: SVN-Gilroy,sans-serif;
      font-size: 18px;
      font-style: normal;
      font-weight: 700;
      line-height: 157.9%;
      margin: 0 34px 5px 34px;
      text-align: center;
      @media screen and (min-width: 826px) {
        font-size: 30px;
      }
    }
    .price-car{
      background:linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
      color: #FFF;
      font-size: 19.6px;
      font-style: normal;
      font-weight: 700;
      line-height: 157.9%;
      text-align: center;
      width: 134px;
      margin: 0 auto;
      @media screen and (min-width: 826px) {
        font-size: 30px;
      }
      span{
        line-height: 5px;
        width: 0.4em;
        border-bottom: 1px solid #000;
        display: inline-block;
      }
    }
    .descr-car{
      margin: 24px 0 35px 0;
      .more-details{
        margin-left: 5px;
        a{
          color: #DE4C2F;
        }
      }
    }
    .order-block{
      display: flex;
      flex-direction: column;
      .wrapper-number-seats{
        display: flex;
        flex-direction: row;
        justify-content: center;
      }
      .img-people{
        width: 40px;
        height: 40px;
        padding: 10px;
        border-radius: 5px;
        border: 1px solid #DE4C2F;
        margin-right: 9px;
        box-sizing: border-box;
        img{
          width: 100%;

        }
      }
      .number-seats{
        width: 40px;
        height: 40px;
        color: #fff;
        font-size: 18px;
        font-weight: 700;
        line-height: 100%;
        background: #DE4C2F;
        border-radius: 5px;
        margin-right: 33px;
        box-sizing: border-box;
        padding: 10px;
      }
      .order-car-btn{
        width: 100%;
        height: 76px;
        padding: 10px 26px;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        background: linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
        box-shadow: 0px 6px 0px 0px #6B1111, 0px 30px 40px 0px rgba(89, 15, 0, 0.50);
        color: white;
        font-size: 26px;
        font-family: "Soyuz Grotesk",sans-serif;
        border: 0;
        margin-top: 19px;
        margin-bottom: 40px;
      }
    }
</style>