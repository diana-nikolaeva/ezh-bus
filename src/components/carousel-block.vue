<script setup lang="ts">
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import ServiceComponent from '@/App.vue'

const a = [1,2, 3, 4];


</script>

<template>
  <carousel :items-to-show="1.5">
    <slide v-for="slide in a" :key="slide">
<!--      {{ slide }}-->
      <service-component></service-component>
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
</template>

