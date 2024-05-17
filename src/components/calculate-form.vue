<script setup lang="ts">
</script>
<template>
  <div class="form-container">
    <form action="" class="calculate-form">
      <input  type="text" placeholder="Как Вас зовут?">
      <input placeholder="Ваш телефон или почта">
      <select name="services" id="">
        <option>Развозка сотрудников</option>
        <option>Детские перевозки</option>
        <option>Аренда авто</option>
        <option>Обслуживание мероприятий</option>
        <option>Трансферные перевозки</option>
        <option>Туристическая развозка</option>
      </select>
      <input type="text" placeholder="Удобное время для звонка">
      <textarea placeholder="Оставьте свой комментарий"></textarea>
      <button class="calc-btn" type="submit">рассчитать</button>
    </form>
    <div class="form-descr">Мы скоро свяжемся с вами и всё расскажем!</div>
  </div>
</template>
<style scoped>
.form-container{
  background: linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
  padding: 44px 27px 31px 27px;
  input, select, textarea{
    height: 56px;
    border-radius: 6px;
    background: #F2F2F2;
    width: 100%;
    color:  #232323;
    font-family: SVN-Gilroy,sans-serif;
    font-size: 16px;
    font-style: normal;
    font-weight: 300;
    line-height: 180.9%;
    margin-bottom: 20px;
    border: 0;
    box-sizing: border-box;
    padding-left: 20px;
  }
  textarea{
    height: 132px;
  }
  .calc-btn{
    width: 100%;
    max-width: 280px;
    height: 76px;
    padding: 10px 26px;
    justify-content: center;
    align-items: center;
    margin-bottom: 40px;
    border-radius: 10px;
    background: radial-gradient(99.74% 133.62% at 1.94% 0%, #FFF 0%, #E7E7E7 49.5%, #D2D2D2 100%);
    box-shadow: 0 6px 0 0 #9B9B9B, 0 30px 40px 0 #590F00;
    color:  #232323;
    text-align: center;
    font-family: "Soyuz Grotesk",sans-serif;
    font-size: 26px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: 1.56px;
    border: 0;
  }
  .form-descr{
    color: #ffffff;
    text-align: center;
    font-family: "Soyuz Grotesk",sans-serif;
    font-size: 18px;
    font-weight: 700;
    margin-bottom: 31px;
  }
}



</style>