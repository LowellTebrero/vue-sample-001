<template>
    <section class="xl:h-[100svh] flex flex-col items-center mt-[3svh] lg:mt-[15svh] gap-y-4 sm:gap-y-[8svh] w-[85%] sm:w-[80%] mx-auto" id="category">
        <TitleSection header="CATEGORY" headertitle="Explore our product" />

        <div class="grid grid-cols-2 sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-4 w-[90%] lg:w-[80%] gap-2 sm:gap-4 lg:gap-10">
            <Card/>
            <Card/>
            <Card/>
            <Card/>
            <Card/>
            <Card/>
            <Card/>
            <Card/>
        </div>

        <div class="">
            <button class="flex items-center text-slate-200 font-extralight hover:-translate-y-2 transition-all text-xs sm:text-sm">
                More product
                    <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24">
                    <path fill="currentColor"
                        d="m13.692 17.308l-.707-.72l4.088-4.088H5v-1h12.073l-4.088-4.088l.707-.72L19 12z" />
                </svg>
            </button>
        </div>
    </section>
</template>

<script setup>
import Card from '@/components/Card.vue';
import TitleSection from '@/components/TitleSection.vue';
</script>

<style scoped></style>