<script setup lang="ts">
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel';
import ServiceComponent from '@/components/service-component.vue'

import { serviceBlocks } from '@/data/services';

function isRed (myIndex: number): boolean {
  return myIndex===2 || myIndex === 5;
}


</script>

<template>
  <carousel
    :wrap-around="true"
    :items-to-show="1"
    :autoplay="2500"
    class="carousel-container">
    <slide v-for="(slide,index) in serviceBlocks" :key="slide">
        <service-component
          class="carousel-service"
          :class="{ red: isRed(index) }"
          :img-path="slide.imgBcgr"
          :link="slide.link"
          :title="slide.title"
          :description="slide.description"
        ></service-component>
    </slide>
  </carousel>
</template>

<style>

.carousel-service {
  background: #1B1C1E;
  min-width: 260px;
  width: 100%;
  min-height: 239px;
  height: 100%;
  position: relative;
  text-align: left;
  border: 1px solid #535353;
  border-radius: 10px;
  margin-left: 20px;
  &.red{
    background:linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
    a{
      color: white;
    }
  }


  img{
    position: absolute;
    right: 0;
    bottom: 0;
    max-height: 93%;
  }
  h3{
    color: #FFF;
    font-family: "Soyuz Grotesk",sans-serif;
    font-size: 18px;
    margin-top: 30px;
    width: 50%;
    @media screen and (min-width:400px) {
      font-size: 25px;
    }
  }
  a{
    color:  #DE4C2F;
    font-family: SVN-Gilroy,sans-serif;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    text-decoration-line: underline;
    @media screen and (min-width:400px) {
      font-size: 25px;
    }
  }
}
</style>
