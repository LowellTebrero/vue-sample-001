<template>
    <div class="carousel-container  sm:h-[60vh]">
      <button @click="prevSlide" class="prev-btn">&#10094;</button>
      <div class="carousel md:mt-20">
        <div
          class="slide"
          v-for="(slide, index) in slides"
          :key="index"
          :style="slideStyles(index)"
        >
        <div class="w-[15rem] sm:w-[22rem] lg:w-[23rem] xl:w-[27rem]  2xl:w-[34rem]">
            <router-link to="/product">
              <img src="/src/assets/img/no-bg-img.png" :alt="`Slide ${index + 1}`">
            </router-link>
        </div>
        </div>
      </div>
      <button @click="nextSlide" class="next-btn">&#10095;</button>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const props = defineProps({
    slides: {
      type: Array,
      required: true,
      validator: slides => {
        return slides.every(slide =>
          typeof slide.image === 'string' &&
          (typeof slide.style === 'object' || typeof slide.style === 'undefined') &&
          (typeof slide.class === 'string' || typeof slide.class === 'undefined')
        );
      }
    }
  });
  
  const currentIndex = ref(0);
  
  const slideStyles = index => {
    const totalSlides = props.slides.length;
    const position = ((index - currentIndex.value) + totalSlides) % totalSlides;
    let translateX = 0;
    let scale = 1;
    let zIndex = 1;
    let opacity = 1;
  
    if (position === 0) {
      translateX = 0;
      scale = 1;
      zIndex = 2;
      opacity = 1;
    } else if (position === 1 || position === totalSlides - 1) {
      translateX = position === 1 ? 120 : -120;
      scale = 0.7;
      zIndex = 1;
      opacity = 0.5;
    } else {
      opacity = 0;
    }
  
    return {
      transform: `translateX(${translateX}%) scale(${scale})`,
      opacity: opacity,
      zIndex: zIndex
    };
  };
  
  const prevSlide = () => {
    currentIndex.value = (currentIndex.value - 1 + props.slides.length) % props.slides.length;
  };
  
  const nextSlide = () => {
    currentIndex.value = (currentIndex.value + 1) % props.slides.length;
  };
  
  let intervalId;
  
  onMounted(() => {
    intervalId = setInterval(nextSlide, 3000); // Change slide every 3 seconds
  });
  
  onUnmounted(() => {
    clearInterval(intervalId);
  });
  </script>
  
  <style scoped>
  .carousel-container {
    position: relative;
    width: 80%;
    max-width: 1300px;
    margin: 0 auto;
    overflow: hidden;
  }
  
  .carousel {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    height: 400px;
  }
  
  .slide {
    position: absolute;
    transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out;
  }
  
  .slide img {
    width: 100%;
    height: auto;
  }
  
  .prev-btn, .next-btn {
    position: absolute;
    top: 50%;
    background: rgba(0, 0, 0, 0.5);
    color: #fff;
    border: none;
    padding: 10px;
    cursor: pointer;
    z-index: 2;
  }
  
  .prev-btn {
    left: 10px;
  }
  
  .next-btn {
    right: 10px;
  }
  
  .prev-btn:hover, .next-btn:hover {
    background: rgba(0, 0, 0, 0.8);
  }
  </style>
  