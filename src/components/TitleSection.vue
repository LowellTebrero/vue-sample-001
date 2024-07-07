<template>
    <div class="flex items-center  flex-col">
        <h4 class="font-extralight">{{ props.header }}</h4>
        <h2 class="tracking-wide text-lg sm:text-2xl">{{ props.headertitle }}</h2>
    </div>
</template>

<script setup>
    const props = defineProps([
        "header",
        "headertitle"
    ])
</script>
