<template>
     <section class="sm:h-[90svh] flex flex-col items-center overflow-hidden mt-[5svh] sm:mt-[15svh] gap-y-5 sm:gap-y-[10svh]" id="product">
    <TitleSection header="OUR PRODUCT" headertitle="Latest clothing design"/> 
    <div class="sm:h-[70vh] w-full">
      <Carousel :slides="carouselSlides" />
    </div>
  </section>
</template>

<script setup>

import TitleSection from '@/components/TitleSection.vue';
import Carousel from '@/components/Carousel.vue';
import { ref } from 'vue';


const carouselSlides = ref([
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' },
  { image: '/assets/img/no-bg-img.png' }
]);

</script>

