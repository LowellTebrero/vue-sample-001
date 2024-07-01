<template>
    <section class="sm:h-[95svh] flex flex-col items-center sm:overflow-hidden mt-[3svh] lg:mt-[15svh] gap-y-5  sm:gap-y-[5svh] md:gap-y-[10svh] w-[85%] sm:w-[80%] mx-auto" id="qualityfirst">
        <TitleSection header="QUALITY FIRST" headertitle="Quality of our clothing" />

        <p class="text-justify sm:text-center font-extralight text-xs sm:text-sm lg:text-base">
            Life is a journey filled with ups and downs, but each moment is a chance to grow and learn. Embrace
            challenges as opportunities to become stronger and wiser. Believe in your dreams, and take small steps each
            day towards achieving them. Surround yourself with positive people who uplift and inspire you.
        </p>

        <div class="flex flex-col sm:flex-row w-full sm:h-[50vh] text-zinc-300">
            <div class="flex-1 flex items-center justify-center py-5 sm:py-0">
                <img src="/src/assets/img/image.png" alt="image" width="200" class="floating sm:w-[25rem]">
            </div>

            <div class="flex-1 flex flex-col items-end pl-[1rem] lg:pl-[5rem] gap-y-10  justify-center">

                <div class="flex justify-between items-center space-x-4">
                    <div>
                        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
                            <g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                stroke-width="2">
                                <path d="M11 12a1 1 0 1 0 2 0a1 1 0 1 0-2 0" />
                                <path d="M12 7a5 5 0 1 0 5 5" />
                                <path d="M13 3.055A9 9 0 1 0 20.941 11" />
                                <path d="M15 6v3h3l3-3h-3V3zm0 3l-3 3" />
                            </g>
                        </svg>
                    </div>
                    <div>
                        <h3 class=" text-sm sm:text-base lg:text-xl">100% Clothing</h3>
                        <p class=" font-extralight text-xs lg:text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem
                            nesciunt corporis provident
                            necessitatibus beatae, at facere deleniti sed sequi commodi?
                        </p>
                    </div>
                </div>

                <div class="flex justify-between items-center space-x-4">
                    <div>
                        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
                            <path fill="currentColor"
                                d="M6 23H3q-.825 0-1.412-.587T1 21v-3h2v3h3zm12 0v-2h3v-3h2v3q0 .825-.587 1.413T21 23zm-6-4.5q-3 0-5.437-1.775T3 12q1.125-2.95 3.563-4.725T12 5.5t5.438 1.775T21 12q-1.125 2.95-3.562 4.725T12 18.5m0-2q2.2 0 4.025-1.2t2.8-3.3q-.975-2.1-2.8-3.3T12 7.5T7.975 8.7t-2.8 3.3q.975 2.1 2.8 3.3T12 16.5m0-1q1.45 0 2.475-1.025T15.5 12t-1.025-2.475T12 8.5T9.525 9.525T8.5 12t1.025 2.475T12 15.5m0-2q-.625 0-1.063-.437T10.5 12t.438-1.062T12 10.5t1.063.438T13.5 12t-.437 1.063T12 13.5M1 6V3q0-.825.588-1.412T3 1h3v2H3v3zm20 0V3h-3V1h3q.825 0 1.413.588T23 3v3zm-9 6" />
                        </svg>
                    </div>
                    <div>
                        <h3 class=" text-sm sm:text-base lg:text-xl">Authenticity</h3>
                        <p class=" font-extralight text-xs lg:text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem
                            nesciunt corporis provident
                            necessitatibus beatae, at facere deleniti sed sequi commodi?
                        </p>
                    </div>
                </div>

                <div class="flex justify-between items-center space-x-4">
                    <div>
                        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 48 48">
                            <g fill="none">
                                <path
                                    d="M21.37 36c1.45-5.25 6.52-9 12.36-8.38c5.56.59 9.98 5.28 10.26 10.86c.07 1.47-.13 2.88-.56 4.19c-.26.8-1.04 1.33-1.89 1.33H11.758c-5.048 0-8.834-4.619-7.844-9.569L10 4h12l4 7l-8.57 6.13L15 14" />
                                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                    stroke-miterlimit="2" stroke-width="4"
                                    d="M21.37 36c1.45-5.25 6.52-9 12.36-8.38c5.56.59 9.98 5.28 10.26 10.86c.07 1.47-.13 2.88-.56 4.19c-.26.8-1.04 1.33-1.89 1.33H11.758c-5.048 0-8.834-4.619-7.844-9.569L10 4h12l4 7l-8.57 6.13L15 14m2.44 3.13L22 34" />
                            </g>
                        </svg>
                    </div>
                    <div>
                        <h3 class=" text-sm sm:text-base lg:text-xl">Quality Matters</h3>
                        <p class=" font-extralight text-xs lg:text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem
                            nesciunt corporis provident
                            necessitatibus beatae, at facere deleniti sed sequi commodi?
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
    import TitleSection from '@/components/TitleSection.vue';
</script>

<style scoped>
.floating {
    animation: float 3s ease-in-out infinite;
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