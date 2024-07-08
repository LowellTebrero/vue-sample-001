<template>
    <section class="xl:h-[70svh] flex flex-col items-center overflow-hidden  mt-[10svh] lg:mt-[15svh] w-[85%] sm:w-[80%] mx-auto text-slate-200 " id="about">
        <div ref="about" style="pointer-events: none;" class="h-[10vh] md:h-[15vh] xl:h-[20vh]"></div>
        <TitleSection header="ABOUT US" headertitle="Learn about us" />

        <div class="flex flex-col md:flex-row h-full mt-[10vh]">
            <div class="w-full flex items-center justify-center h-[50vh] relative">
                <div class="w-[50%] bg-zinc-500 h-[25vh] xl:h-[30vh] absolute left-16 sm:left-20 md:left-5 lg:left-5 xl:left-16 top-5 rounded-lg overflow-hidden hover:z-40 ease-out duration-300 hover:scale-[115%]">
                    <img src="/src/assets/img/BASIC.jpg" class="object-cover object-center w-full h-full " alt="">
                     
                </div>
                <div class="w-[50%]  bg-zinc-900 h-[25vh] xl:h-[30vh] relative  rounded-lg  overflow-hidden hover:z-40 ease-out duration-300 hover:scale-[115%]">
                    <span class="w-full absolute bg-gradient-to-t from-neutral-800 from-10% hover:bg-none ease-out duration-300 h-full"></span>
                    <img src="/src/assets/img/profile.jpg" class="object-cover object-center w-full h-full" alt="">
                </div>

            </div>
            <div class="w-full flex flex-col gap-y-2">
                <h2 class="tracking-wide text-base lg:text-lg">WHAT YOU SEE IS WHAT YOU GET</h2>
                <p class="font-extralight text-xs lg:text-sm xl:text-base text-justify sm:text-left">
                    design involves the art and process of creating garments that are not only functional but also
                    aesthetically pleasing. Designers typically consider factors such as fabric selection, garment
                    construction techniques, color theory, and trends in fashion. Their goal is to create clothing that
                    fits well, is comfortable, and expresses the desired style or message for the wearer. Successful
                    clothing design often combines creativity with technical skill to produce pieces that are both
                    innovative and commercially viable. <br/> <br/>

                    design involves the art and process of creating garments that are not only functional but also
                    aesthetically pleasing. Designers typically consider factors such as fabric selection, garment
                    construction techniques, color
                </p>
            </div>
        </div>
    </section>
</template>

<script setup>
import TitleSection from '@/components/TitleSection.vue';

</script>

<style scoped></style>