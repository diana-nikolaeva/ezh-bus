<script>
import { defineComponent } from 'vue'
import CalculateForm from '@/components/calculate-form.vue'

export default defineComponent({
  components: { CalculateForm }
})
</script>
<template>
  <div class="calculate-block-container">
    <div class="title-block">
      <h3>Калькулятор стоимости вашей поездки</h3>
      <img src="../assets/calc-bcgr.png" alt="calculate">
    </div>
    <div class="title-descr">Сообщите нашей компании маршрут и время подачи транспорта для перевозки</div>|
  </div>
  <calculate-form></calculate-form>
</template>

<style scoped>
  .calculate-block-container{
    .title-block{
      margin: 20px;
      border-radius: 10px;
      border: 1px solid #535353;
      background: #1B1C1E;
      position: relative;
      height: 296px;
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
    .title-descr{
      margin: 0 20px;
      color:  #232323;
      text-align: center;
      font-family: SVN-Gilroy,sans-serif;
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
    }
  }
</style>