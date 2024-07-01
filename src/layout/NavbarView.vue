<template>
    <div class="flex justify-between items-center h-[8svh] w-[80%] mx-auto transition-all">
        <h3>Lroom</h3>
        <div class="hidden lg:block">
            <ul class="flex font-extralight">
                <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#home">Home</a></li>
                <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#product">Product</a>
                </li>
                <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm"
                        href="#qualityfirst">Quality</a></li>
                <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm"
                        href="#category">Category</a></li>
                <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#about">About Us</a>
                </li>
                <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#contact">Contact</a>
                </li>
            </ul>
        </div>

        <div class="block lg:hidden">
            <button @click="toggleSidebar" class="z-50 relative">
                <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 15 15">
                    <path fill="currentColor" fill-rule="evenodd"
                        d="M1.5 3a.5.5 0 0 0 0 1h12a.5.5 0 0 0 0-1zM1 7.5a.5.5 0 0 1 .5-.5h12a.5.5 0 0 1 0 1h-12a.5.5 0 0 1-.5-.5m0 4a.5.5 0 0 1 .5-.5h12a.5.5 0 0 1 0 1h-12a.5.5 0 0 1-.5-.5"
                        clip-rule="evenodd" />
                </svg>
            </button>

            <div :class="{ 'sidebar': true, 'sidebar-open': isOpen }">

                <div class="sidebar-content">
                    <!-- Your sidebar content here -->
                    <ul class="flex font-extralight gap-y-10 flex-col">
                        <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#home">Home</a></li>
                        <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#product">Product</a>
                        </li>
                        <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm"
                                href="#qualityfirst">Quality</a></li>
                        <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm"
                                href="#category">Category</a></li>
                        <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#about">About Us</a>
                        </li>
                        <li><a class="hover:bg-zinc-700 py-3 px-5 rounded-lg transition-all text-sm" href="#contact">Contact</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const isOpen = ref(false);

const toggleSidebar = () => {
    isOpen.value = !isOpen.value;
};
</script>

<style>
.sidebar {
    position: fixed;
    top: 0;
    right: -200px;
    width: 200px;
    height: 100%;
    background: #333;
    color: white;
    transition: right 0.3s ease;
    overflow: hidden;
    padding: 20px;
    box-sizing: border-box;
}

.sidebar-open {
    right: 0;
}


.sidebar-open .sidebar-toggle {
    right: 200px;
}

.sidebar-content {
    margin-top: 50px;
}
</style>
