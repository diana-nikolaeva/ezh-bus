<script setup lang="ts">
</script>
<template>
  <div class="form-container">
    <form action="" class="calculate-form">
      <div class="input-wrapper">
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
      </div>
      <div class="btn-wrapper">
        <button class="calc-btn btn" type="submit">рассчитать</button>
        <div class="form-descr">Мы скоро свяжемся с вами и всё расскажем!</div>
      </div>
    </form>

  </div>
</template>
<style scoped>
.form-container{
  background: linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
  padding: 44px 27px 31px 27px;
  @media only screen and (min-width: 865px){
    flex-grow: 1;
    border-radius: 10px;
    border: 1px solid #535353;
    padding: 44px 34px 24px 53px;
  }
  .calculate-form{
    @media only screen and (min-width: 865px){
      display: flex;
      flex-direction: row;
      align-items: flex-end;
    }
  }
  .input-wrapper{
    @media only screen and (min-width: 865px){
      width: 66%;
      display: flex;
      flex-wrap: wrap;
      flex-direction: column;
      height: 230px;
      align-items: stretch;
    }
  }
  .btn-wrapper{
    @media only screen and (min-width: 865px){
      width: 33%;
      display: flex;
      flex-direction: column-reverse;
    }
  }
  textarea{
    height: 132px;
    @media only screen and (min-width: 865px){
      margin-right: 20px;
      width: 46%;
    }
  }
  input, select{
    @media only screen and (min-width: 865px){
      margin-right: 20px;
      width: 46%;
    }
  }
  .calc-btn{
    margin-bottom: 40px;
    background: radial-gradient(99.74% 133.62% at 1.94% 0%, #FFF 0%, #E7E7E7 49.5%, #D2D2D2 100%);
    box-shadow: 0 6px 0 0 #9B9B9B, 0 30px 40px 0 #590F00;
    color:  #232323;
    @media only screen and (min-width: 865px){
      margin-bottom: 35px;
    }
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