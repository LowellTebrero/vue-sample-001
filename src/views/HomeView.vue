<template>

  <header class="z-50 fixed w-full" :class="{ color: isSticky }">
    <NavbarView />
  </header>

  <main class="w-[85%] sm:w-[80%] mx-auto text-slate-200 relative">
    <!-- Hero Section -->
    <HeroSection/>
  </main>

  <!-- Headline Section -->
   <HeadlineSection/>

  <!-- Our Product Section -->
  <OurProductSection/>
 

  <!-- About Clothing Section -->
  <AboutClothingSection/>

  <!-- Category Section -->
  <CategorySection/>


  <!-- About Us Section -->
  <AboutUsSection/>

  <!-- Footer Section -->
  <FooterSection/>

</template>

<script setup>
import NavbarView from '@/layout/NavbarView.vue';
import HeroSection from '@/layout/HeroSection.vue';
import HeadlineSection from '@/layout/HeadlineSection.vue';
import AboutClothingSection from '@/layout/AboutClothingSection.vue';
import OurProductSection from '@/layout/OurProductSection.vue';
import CategorySection from '@/layout/CategorySection.vue';
import AboutUsSection from '@/layout/AboutUsSection.vue';
import FooterSection from '@/layout/FooterSection.vue';

import { ref, onMounted, onBeforeUnmount } from 'vue';

const isSticky = ref(false);

const handleScroll = () => {
  isSticky.value = window.scrollY > 200;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});

</script>



<style>
.color {
  /* Add your sticky styles here */
  background-color: #131313; /* Example style */
  transition: all .2s ease-in;
}
</style>