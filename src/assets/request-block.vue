<script setup lang="ts">

</script>

<template>
  <section class="request-block">
    <h2>оставить заявку</h2>
    <div class="descr">Заказывая автотранспортные услуги в нашей компании, вы получаете комфортную и надежную перевозку по оптимальной цене </div>
    <form action="">
      <input type="text" placeholder="Как Вас зовут?">
      <input placeholder="Ваш телефон или почта">
      <button type="submit" class="request-btn btn">оставить заявку</button>
    </form>
    <div class="person-data">Нажимая на кнопку "Отправить”, я соглашаюсь условиями обработки персональных данных</div>
  </section>
</template>

<style scoped>
  .request-block {
    background: linear-gradient(114deg, #3F3F3F 1.43%, #111 101.61%);
    padding: 0 20px;
    color: #fff;

    h2 {
      padding-bottom: 20px;
      color: #fff;
    }

    .descr {
      text-align: center;
    }

    form {
      margin-top: 25px;
    }

    .request-btn {
      background: linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
      box-shadow: 0 6px 0 0 #6B1715, 0 30px 40px 0 #010101;
      color: #fff;
      margin-top: 7px;
      margin-bottom: 36px;
      padding: 10px 20px;
    }

    .person-data {
      color: #8C8C8C;
      text-align: center;
      font-family: 'SF Compact Display', sans-serif;
      font-size: 12px;
      font-style: normal;
      font-weight: 400;
      line-height: 130%;
      margin-bottom: 20px;
    }
  }

</style>