<template>
   <div class="card w-full h-full overflow-hidden rounded-sm flex flex-col items-center justify-center gap-y-4  lg:h-[30svh]">
      <div class="img-wrapper">
         <img class="sm:w-[13rem]" src="/src/assets/img/no-bg-img.png" alt="image">
      </div>
        <h3 class="font-extralight title text-xs sm:text-sm lg:text-lg">{{ props.title }}</h3>
   </div>
</template>

<script setup>

const props = defineProps([
      "title"
    ])
</script>


<style scoped>
  .card {
      position: relative;
      overflow: hidden;
      border-radius: 10px;
      text-align: center;
      transition: all 0.3s ease-in-out;
      border: 1px solid #696969;
      padding: 1rem;
    }

    .card img {
      height: auto;
      transition: width 0.3s ease-in-out;
    }

    .card .title {
      position: absolute;
      bottom: 10px;
      left: 50%;
      transform: translateX(-50%);
      transition: bottom 0.3s ease-in-out;
      padding: 0.5rem;
      border-radius: 5px;
    }

    .card:hover img {
      width: 18rem;
      animation: float 3s ease-in-out infinite;
    }

    .card:hover .title {
      bottom: 2rem;
    }

    @keyframes float {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-10px);
      }
    }
</style>