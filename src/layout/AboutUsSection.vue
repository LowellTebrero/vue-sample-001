<template>
    <section class="lg:h-[70svh] flex flex-col items-center overflow-hidden mt-[10svh] lg:mt-[15svh] w-[85%] sm:w-[80%] mx-auto text-slate-200" id="about">
        <TitleSection header="ABOUT US" headertitle="Learn about us" />

        <div class="flex flex-col sm:flex-row w-full h-full mt-[10vh]">
            <div class="flex-1 flex relative animate-left">
                <div class="lg:w-[40%] bg-zinc-500 h-[30vh] sm:absolute left-4 top-5 rounded-lg overflow-hidden hover:z-40 ease-out duration-300 hover:scale-[115%]">
                    <img src="/src/assets/img/BASIC.jpg" class="object-cover object-center w-full h-full " alt="">
                </div>
                <div class="lg:w-[40%] bg-zinc-900 h-[30vh] sm:absolute left-[6rem]  rounded-lg top-20 overflow-hidden hover:z-40 ease-out duration-300 hover:scale-[115%]">
                    <span class="w-full absolute bg-gradient-to-t from-neutral-800 from-10% hover:bg-none ease-out duration-300 h-full"></span>
                    <img src="/src/assets/img/profile.jpg" class="object-cover object-center w-full h-full" alt="">
                </div>
            </div>
            <div class="flex-1 flex  flex-col gap-y-2 sm:pl-5 mt-[5vh] sm:mt-0 animate-right">
                <h2 class="tracking-wide text-base lg:text-lg">WHAT YOU SEE IS WHAT YOU GET</h2>
                <p class="font-extralight text-xs sm:text-sm lg:text-base text-justify sm:text-left">
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