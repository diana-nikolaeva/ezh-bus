<script>
import { defineComponent } from 'vue'
import CalculateForm from '@/components/calculate-form.vue'

export default defineComponent({
  components: { CalculateForm }
})
</script>
<template>
  <div class="title-descr">Сообщите нашей компании маршрут и время подачи транспорта для перевозки</div>
  <div class="calculate-block-container">
    <div class="title-block">
      <h3>Калькулятор стоимости вашей поездки</h3>
      <img src="../assets/calc-bcgr.png" alt="calculate">
    </div>
    <calculate-form></calculate-form>
  </div>

</template>

<style scoped>
  .calculate-block-container{
    max-width: 1250px;
    margin: 0 auto;
    @media only screen and (min-width: 865px){
      display: flex;
      flex-direction: row;
    }
    .title-block{
      margin: 20px;
      border-radius: 10px;
      border: 1px solid #535353;
      background: #1B1C1E;
      position: relative;
      height: 296px;
      @media only screen and (min-width: 865px){
        width: 300px;
        margin: 0;
        box-sizing: border-box;
        margin-right: 20px;
        flex-grow: 0;
      }
      h3{
        color:  #FFF;
        font-family: "Soyuz Grotesk",sans-serif;
        font-size: 30px;
        font-style: normal;
        font-weight: 700;
        margin-top: 39px;
        margin-left: 46px;
        margin-bottom: 20px;
      }
      img{
        max-height: 100%;
        position: absolute;
        bottom: 0;
        right: 0;
      }
    }
  }

  .title-descr{
    margin: 0 20px;
    color:  #232323;
    text-align: center;
    font-family: SVN-Gilroy,sans-serif;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    @media only screen and (min-width: 865px){
      margin-bottom: 70px;
      margin-top: 50px;
      font-size: 30px;
      text-align: center;
    }
  }
</style>