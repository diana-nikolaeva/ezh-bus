<script setup lang="ts">
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide } from 'vue3-carousel';
import CarComponent from '@/components/car-component.vue';
import {ourCars } from '@/data/cars';

defineProps({ isPhone: Boolean });
</script>

<template>
<section class="our-cars">
  <h2>наш автопарк</h2>
  <div class="container-car-block">
    <carousel
      :wrap-around="true"
      :items-to-show="1"
      :autoplay="1500"
      v-if="isPhone"
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
    <template v-else>
      <car-component
        class="card-of-car"
        v-for="item in ourCars" :key="item"
        :img-path="item.imgPath"
        :title="item.title"
        :price="item.price"
        :descr="item.descr"
        :seats="item.seats"
      ></car-component>
    </template>
  </div>
</section>
</template>

<style scoped>
  .our-cars{
    background: #DE4C2F;
    padding: 0  20px 19px 20px;
    h2{
      color: #fff;
      padding-bottom: 0;
    }
  }
  .container-car-block{
    @media only screen and (min-width: 845px){
      max-width: 1250px;
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      margin: 0 auto;
    }
    .card-of-car{
      background: #fff;
      border-radius: 10px;
      box-sizing: border-box;
      padding: 29px 26px 0 26px;
      max-width: 403px;
      margin-right: 20px;
      margin-top: 20px;
      &:last-child{
       margin-right: 0;
      }
    }
  }
</style>