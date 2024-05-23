<template>
  <section class="our-services">
    <h2>услуги.</h2>
    <!--  <div class="container">контейнер для блока услуг на десктопе</div>-->
    <CarouselBlock v-if="isPhone"></CarouselBlock>
    <div class="container"  v-else>
      <service-component v-for="item in serviceBlocks"
                         :key="item"
                         :img-path= "item.imgBcgr"
                         :link="item.link"
                         :title="item.title"
      ></service-component>
    </div>
  </section>

</template>

<style>

  h2{
    padding-bottom: 22px;
  }
  .container {
    max-width: 1250px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: 0 auto;
    justify-content: center;
  }

</style>
<script setup lang="ts">
import ServiceComponent from '@/components/service-component.vue'
import {serviceBlocks} from '@/data/services';
import CarouselBlock from '../components/carousel-block.vue';

defineProps({ isPhone: Boolean });


</script>
