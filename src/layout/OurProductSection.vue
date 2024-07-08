<template>
     <section class="sm:h-[90svh] flex flex-col items-center overflow-hidden mt-[5svh] sm:mt-[15svh] gap-y-5 sm:gap-y-[10svh]"
      id="product">
      <div ref="product" style="height: 50px;  top: -50px; pointer-events: none;"></div>
    <TitleSection header="OUR PRODUCT" headertitle="Latest clothing design"/> 
    <div class="sm:h-[70vh] w-full animate-top">
      <Carousel :slides="carouselSlides" :showModal="showModal" />
    </div>
  </section>

  <Modal
    v-show="currentModal"
    @close="closeModal"
    @click="closeOnClickOutside">
    <template v-slot:header>
        <h4 class="font-extralight tracking-wide">View Product</h4>
    </template>

    <template v-slot:body>

      <section class="w-auto sm:w-[80%] mx-auto flex flex-col md:flex-row  relative pb-10">
        <div class="flex-1 w-full flex items-center justify-center">
            <div class="w-[15rem] lg:w-[25rem]">
                <img src="/src/assets/img/no-bg-img.png" alt="">
            </div>
        </div>
        <div class="flex-1 w-full flex items-center md:items-start flex-col gap-y-5 pt-[4vh]">

            <h1 class="tracking-wide font-medium lg:text-5xl">NIMBUS</h1>
            <p class="font-extralight text-xs lg:text-base text-center md:text-left">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem
                Ipsum has been the
                industry's standard dummy text ever since the 1500s,</p>
            <h4 class="font-extralight tracking-wide text-xs lg:text-base">AVAILAIBLE SIZE: XL, LG, SM, XS</h4>
            <h4 class="font-extralight tracking-wide text-xs lg:text-base">PRICE: 300.00 PHP</h4>
            <h4 class="font-extralight tracking-wide text-xs lg:text-base">COLOR: BLACK</h4>

            <div class="md:mt-[5vh] xl:mt-[5vh] space-x-5 flex w-[7rem]">
                <button class="rounded-full bg-neutral-500 w-full">&nbsp;</button>
                <button class="rounded-full bg-red-500 w-full">&nbsp;</button>
                <button class="rounded-full bg-yellow-500 w-full">&nbsp;</button>
            </div>
        </div>

    </section>

        
    </template>              
  </Modal>
</template>

<script setup>


import TitleSection from '@/components/TitleSection.vue';
import Carousel from '@/components/Carousel.vue';
import { ref } from 'vue';
import Modal from '@/components/Modal.vue';

const currentModal = ref(false);

const  showModal = () => {
  currentModal.value = true;   
};

const closeModal = () => {
  currentModal.value = false; 
};

const closeOnClickOutside = (event) => {
  if (event.target.classList.contains('modal-backdrop')) {
      currentModal.value = false;       
  }
};


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

