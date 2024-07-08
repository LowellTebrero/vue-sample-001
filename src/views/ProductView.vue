<template>
    <section class="w-[85%] sm:w-[80%] mx-auto pt-[10vh] flex flex-col md:flex-row  2xl:h-[90vh] relative">
        <router-link to="/#product" class="absolute lg:top-[10vh] right-4">
            <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 1024 1024">
                <path fill="currentColor"
                    d="M609.408 149.376L277.76 489.6a32 32 0 0 0 0 44.672l331.648 340.352a29.12 29.12 0 0 0 41.728 0a30.592 30.592 0 0 0 0-42.752L339.264 511.936l311.872-319.872a30.592 30.592 0 0 0 0-42.688a29.12 29.12 0 0 0-41.728 0z" />
            </svg>
        </router-link>
        <a href="/#product" class="absolute lg:top-[10vh] right-4">X</a>
        <div class="flex-1 w-full flex items-center justify-center">
            <div class="w-[20rem] lg:w-auto">
                <img src="/src/assets/img/no-bg-img.png" alt="">
            </div>
        </div>
        <div class="flex-1 w-full flex items-center md:items-start flex-col gap-y-5 pt-[10vh]">

            <h1 class="tracking-wide font-medium lg:text-5xl">NIMBUS</h1>
            <p class="font-extralight text-xs lg:text-base text-center md:text-left">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem
                Ipsum has been the
                industry's standard dummy text ever since the 1500s,</p>
            <h4 class="font-extralight tracking-wide text-xs lg:text-base">AVAILAIBLE SIZE: XS, SM, M, L, XL</h4>
            <h4 class="font-extralight tracking-wide text-xs lg:text-base">PRICE: 300.00 PHP</h4>
            <h4 class="font-extralight tracking-wide text-xs lg:text-base">COLOR: BLACK</h4>

            <div class="md:mt-[5vh] xl:mt-[20vh] space-x-5 flex w-[7rem]">
                <button class="rounded-full bg-neutral-500 w-full">&nbsp;</button>
                <button class="rounded-full bg-red-500 w-full">&nbsp;</button>
                <button class="rounded-full bg-yellow-500 w-full">&nbsp;</button>
            </div>
        </div>

    </section>
</template>

<script setup>

</script>

<style scoped></style>