<template>
    <div class="mt-[5vh] sm:mt-0 h-[5svh] bg-zinc-800 flex items-center justify-evenly px-5 font-extralight positioning overflow-hidden">
        <h4 class="marquee text-sm sm:text-base">Royalty free - keep everything you earn</h4>
        <h4 class="marquee text-sm sm:text-base">100% Cloth - want you what you leave</h4>
        <h4 class="marquee text-sm sm:text-base">Quality - Affordable and Quality first</h4>
    </div>
</template>


<style scoped>

.positioning {
    position: relative;
}
.marquee {
    position: absolute;
    right: -20rem;
    animation: marquee 10s linear infinite;
}

h4:nth-child(1) {
    animation-delay: 0s;
}

h4:nth-child(2) {
    animation-delay: 3.33s;
}

h4:nth-child(3) {
    animation-delay: 6.66s;
}

@keyframes marquee {
    0% { transform: translateX(0%); }
    100% { transform: translateX(-800%); }
}

</style>