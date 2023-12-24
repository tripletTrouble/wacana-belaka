<script setup>
    const props = defineProps({
        text: String,
        link: String
    })
</script>

<template>
    <a class="block w-full text-center py-4 font-semibold text-sm text-sky-500 active:text-sky-300" :href="link">{{ text }}</a>
</template>