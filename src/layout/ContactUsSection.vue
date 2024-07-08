<template>
     <section class="lg:h-[80svh] flex flex-col items-center overflow-hidden mt-[10svh] lg:mt-[15svh] w-[85%] sm:w-[80%] mx-auto text-slate-200" id="contact">
        <TitleSection header="CONTACT" headertitle="Connect with us"/>

        <div class="mt-[15svh] space-y-4 w-full lg:w-1/3 2xl:w-1/2 animate-top">
            <div>
                <label for="name">Name</label>
                <input type="text" class="block bg-transparent border px-4 py-2 w-full rounded text-xs sm:text-sm lg:text-base" placeholder="Type your name here" id="name">
            </div>
            <div>
                <label for="email">Email or number</label>
                <input type="text" class="block bg-transparent border px-4 py-2 w-full rounded text-xs sm:text-sm lg:text-base" placeholder="Type your email or number here" id="email">
            </div>
            <div>
                <label for="messages">Messages here</label>
                <textarea name="" id="messages" cols="30" rows="10" class="text-xs sm:text-sm lg:text-base block bg-transparent border px-4 py-2 w-full rounded" placeholder="Type your messages here" ></textarea>
            </div>
            <button class="bg-zinc-800 px-4 py-2 rounded-md text-xs sm:text-sm lg:text-base">Send here</button>
        </div>
    </section>
</template>

<script setup>
import TitleSection from '@/components/TitleSection.vue';

</script>

<style scoped>

</style>