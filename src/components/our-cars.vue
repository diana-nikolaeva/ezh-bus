<script setup lang="ts">
import { Carousel, Slide } from 'vue3-carousel'
import CarComponent from '@/components/car-component.vue'
import {ourCars } from '@/data/cars'

defineProps({ isPhone: Boolean });
</script>

<template>
<section class="our-cars">
  <h2>наш автопарк</h2>
  {{isPhone}}
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
    <car-component
      v-else
      v-for="item in ourCars" :key="item"
      :img-path="item.imgPath"
      :title="item.title"
      :price="item.price"
      :descr="item.descr"
      :seats="item.seats"
    ></car-component>
  </div>
</section>
</template>

<style scoped>
  .our-cars{
    background: #DE4C2F;
    padding: 0  20px 19px 20px;
    h2{
      color: #fff;
      padding-bottom: 19px;
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