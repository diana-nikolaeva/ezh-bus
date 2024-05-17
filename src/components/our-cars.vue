<script setup lang="ts">
import { Carousel, Slide } from 'vue3-carousel'
import CarComponent from '@/components/car-component.vue'
import car1 from '../assets/cars-img/sprinter.png';
const ourCars = [
    {
      imgPath: car1,
      title: 'Mercedes-Benz Sprinter',
      price: '1300',
      descr: 'Mercedes benz sprinter 223685 – автобус VIP-класса 2021 года выпуска с комбинированным салоном, панорамным люком в крыше, кресла имеют регулировки положений, окна с тонировкой и шторками',
      seats:'19'
    },
     {
      imgPath: car1,
       title: 'Mercedes-Benz Sprinter',
       price: '1300',
       descr: 'Mercedes benz sprinter 223685 – автобус VIP-класса 2021 года выпуска с комбинированным салоном, панорамным люком в крыше, кресла имеют регулировки положений, окна с тонировкой и шторками',
       seats:'18'
     },
     {
       imgPath: car1,
       title: 'Mercedes-Benz Sprinter',
       price: '1300',
       descr: 'Mercedes benz sprinter 223685 – автобус VIP-класса 2021 года выпуска с комбинированным салоном, панорамным люком в крыше, кресла имеют регулировки положений, окна с тонировкой и шторками',
       seats: '17'
    }
  ]
</script>

<template>
<section class="our-cars">
  <h2>наш автопарк</h2>
  <div class="container-car-block">
    <carousel
      :wrap-around="true"
      :items-to-show="1"
      :autoplay="1500"
      class="carousel-container">
      <slide v-for="slide in ourCars" :key="slide">
        <car-component
          :img-path="slide.imgPath"
          :title="slide.title"
          :price="slide.price"
          :descr="slide.descr"
          :seats="slide.seats"
        ></car-component>
      </slide>
    </carousel>
  </div>
</section>
</template>

<style scoped>
  .our-cars{
    background: #DE4C2F;
    padding: 27px  20px 19px 20px;
    h2{
      color: #fff;
      margin: 0 0 20px 0;
    }
  }
  .container-car-block{
    padding: 29px 26px 0 26px;
    max-width: 403px;
    margin: 0 auto;
    background: #fff;
    border-radius: 10px;
  }
</style>