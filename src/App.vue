<script setup lang="ts">
import HeaderBlock from '@/components/header-block.vue';
import OurServices from '@/components/our-services.vue';
import CalculateBlock from '@/components/calculate-block.vue';
import OurCars from '@/components/our-cars.vue';
import AboutUs from '@/components/about-us.vue';
import ContactsBlock from '@/components/contacts-block.vue';
import RequestBlock from '@/components/footer-block.vue';
import { onMounted, onBeforeUnmount, ref } from 'vue';

const isPhone = ref();

if (typeof window !== 'undefined') {
  const onResize = () => {

    isPhone.value = window.innerWidth <= 865;
  }

  onMounted(() => window.addEventListener('resize', onResize));
  onBeforeUnmount(() => window.removeEventListener('resize', onResize));
  onResize();
}


</script>

<template>
  <header>
    <header-block :is-phone="isPhone"></header-block>
  </header>
  <our-services :is-phone="isPhone"></our-services>
  <calculate-block></calculate-block>
  <our-cars :is-phone="isPhone"></our-cars>
  <about-us></about-us>
  <contacts-block></contacts-block>
  <go-back-btn></go-back-btn>
  <footer>
    <request-block></request-block>
  </footer>
</template>

<style scoped>

</style>
