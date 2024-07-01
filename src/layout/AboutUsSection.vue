<template>
    <section class="lg:h-[90svh] flex flex-col items-center overflow-hidden mt-[10svh] lg:mt-[15svh] w-[85%] sm:w-[80%] mx-auto text-slate-200" id="about">
        <TitleSection header="ABOUT US" headertitle="Learn about us" />

        <div class="flex flex-col sm:flex-row w-full h-full mt-[10vh]">
            <div class="flex-1 flex relative">
                <div class="w-1/2 bg-zinc-500 h-[30vh] sm:absolute left-4 top-5 rounded-lg">1</div>
                <div class="w-1/2 bg-zinc-700 h-[30vh] sm:absolute left-[6rem]  rounded-lg top-20">2</div>
            </div>
            <div class="flex-1 flex  flex-col gap-y-2 sm:pl-5 mt-[5vh] sm:mt-0">
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