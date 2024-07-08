<template>
    
     <section class="sm:h-[90svh] flex flex-col items-center overflow-hidden mt-[5svh] sm:mt-[15svh] gap-y-5 sm:gap-y-[10svh]"
      id="product">
      <div ref="product" style="height: 50px;  top: -50px; pointer-events: none;"></div>
    <TitleSection header="OUR PRODUCT" headertitle="Latest clothing design"/> 
    <div class="sm:h-[70vh] w-full animate-top">
      <Carousel :slides="carouselSlides" />
    </div>
  </section>
</template>

<script setup>

import TitleSection from '@/components/TitleSection.vue';
import Carousel from '@/components/Carousel.vue';
import { ref } from 'vue';


const carouselSlides = ref([
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' },
  { image: 'no-bg-img.png' }
]);

</script>

