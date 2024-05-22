<script setup lang="ts">
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import ServiceComponent from '@/components/service-component.vue'

import img1 from '../assets/service-img/service1.png';
import img2 from '../assets/service-img/service2.png';
import img5 from '../assets/service-img/service5.png';
import img6 from '../assets/service-img/service6.png';
import img7 from '../assets/service-img/service6-phone.png';

const serviceBlocks = [
  {
    imgBcgr: img1,
    title:'развозка сотрудников',
    link:'/',
  },
  {
    imgBcgr: img2,
    title:'детские перевозки',
    link:''
  },
  {
    imgBcgr: '',
    title:'аренда авто с водителем',
    link:''
  },
  {
    imgBcgr: img5,
    title:'трансферные перевозки',
    link:''
  },
  {
    imgBcgr: img6,
    title:'туристическая развозка',
    link:''
  },
  {
    imgBcgr: img7,
    title:'обслуживание мероприятий',
    link:''
  }
];

function isRed (myIndex: number): boolean {
  return myIndex===2 || myIndex === 5;
}


</script>

<template>
  <carousel
    :wrap-around="true"
    :items-to-show="1"
    :autoplay="1500"
    class="carousel-container">
    <slide v-for="(slide,index) in serviceBlocks" :key="slide">
        <service-component
          class="carousel-service"
          :class="{ red: isRed(index) }"
          :img-path="slide.imgBcgr"
          :link="slide.link"
          :title="slide.title"
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
  padding-left: 38px;
  border: 1px solid #535353;
  border-radius: 10px;
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
