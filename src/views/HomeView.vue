<template>

  <header class="z-50 fixed w-full" :class="{ color: isSticky }">
    <NavbarView :scrollToHiddenElement="scrollToHiddenElement" />
  </header>

  <main class="w-[85%] sm:w-[80%] mx-auto text-slate-200 relative">
    <!-- Hero Section -->
    <HeroSection/>
  </main>

  <!-- Headline Section -->
  <HeadlineSection />

  <!-- Our Product Section -->
  <OurProductSection />


  <!-- About Clothing Section -->
  <AboutClothingSection/>

  <!-- Category Section -->
  <CategorySection/>


  <!-- About Us Section -->
  <AboutUsSection/>


  <!-- Contact Us Section -->
  <ContactUsSection/>

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
import ContactUsSection from '@/layout/ContactUsSection.vue';

const isSticky = ref(false);

const handleScroll = () => {
  isSticky.value = window.scrollY > 200;
};

const product = ref(null);
const quality = ref(null);
const category = ref(null);
const about = ref(null);
const contact = ref(null);

const scrollToHiddenElement = () => {
  product.value.scrollIntoView({ behavior: "smooth" });
  quality.value.scrollIntoView({ behavior: "smooth" });
  category.value.scrollIntoView({ behavior: "smooth" });
  about.value.scrollIntoView({ behavior: "smooth" });
  contact.value.scrollIntoView({ behavior: "smooth" });
};


onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});


const checkBoxes = () => {
  const boxes = document.querySelectorAll('.box');
  const animateTop = document.querySelectorAll('.animate-top');
  const animateLeft = document.querySelectorAll('.animate-left');
  const animateRight = document.querySelectorAll('.animate-right');
  const triggerBottom = window.innerHeight / 5 * 4;

  boxes.forEach(box => {
    const boxTop = box.getBoundingClientRect().top;

    if (boxTop < triggerBottom) {
      box.classList.add('show');
    } else {
      box.classList.remove('show');
    }
  });

  animateTop.forEach(box => {
    const boxTop = box.getBoundingClientRect().top;

    if (boxTop < triggerBottom) {
      box.classList.add('show');
    } else {
      box.classList.remove('show');
    }
  });

  animateLeft.forEach(box => {
    const boxLeft = box.getBoundingClientRect().top;

    if (boxLeft < triggerBottom) {
      box.classList.add('show');
    } else {
      box.classList.remove('show');
    }
  });

  animateRight.forEach(box => {
    const boxRight = box.getBoundingClientRect().top;

    if (boxRight < triggerBottom) {
      box.classList.add('show');
    } else {
      box.classList.remove('show');
    }
  });
};

onMounted(() => {
  window.addEventListener('scroll', checkBoxes);
  checkBoxes();
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', checkBoxes);
});

</script>



<style>
.color {
  /* Add your sticky styles here */
  background-color: #131313; /* Example style */
  transition: all .2s ease-in;
}

.box {
  transform: translateY(150%);
  transition: transform .7s ease-in;
  opacity: 0;
  
}
.animate-top {
  transform: translateY(30%);
  transition: transform .7s ease-in;
  opacity: 0;
  
}
.animate-left {
  transform: translateX(-100%);
  transition: transform .7s ease-in;
  opacity: 0;
  
}
.animate-right {
  transform: translateX(100%);
  transition: transform .7s ease-in;
  opacity: 0;
  
}

.box:nth-of-type(even){
  transform: translateY(150%);
  opacity: 0;
}
.animate-top:nth-of-type(even){
  transform: translateY(30%);
  opacity: 0;
}
.animate-left:nth-of-type(even){
  transform: translateX(-100%);
  opacity: 0;
}
.animate-right:nth-of-type(even){
  transform: translateX(100%);
  opacity: 0;
}

.box.show {
  transform: translateY(0);
  animation: showOpacity 4s linear forwards;

}
.animate-top.show {
  transform: translateY(0);
  animation: showOpacity 3s linear forwards;

}
.animate-right.show {
  transform: translateX(0);
  animation: showOpacity 3s linear forwards;

}
.animate-left.show {
  transform: translateX(0);
  animation: showOpacity 3s linear forwards;

}

@keyframes showOpacity {
  0% { opacity: 0%; }
  50% { opacity: 80%; }
  100% { opacity: 100%; }
}
</style>