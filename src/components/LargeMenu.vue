<script setup>
const props = defineProps({
    link: String,
    text: String
})
</script>

<template>
    <a :href="link" class="font-semibold py-1 px-2 lg:px-4 hover:drop-shadow-xl text-sky-500">{{text}}</a>
</template>