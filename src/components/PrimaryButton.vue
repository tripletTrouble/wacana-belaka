<script setup>
const props = defineProps({
    type: {
        default: 'button',
        type: String
    },
    href: {
        default: '#',
        type: String
    }
})
</script>

<template>
    <component :is="type !== 'link' ? 'button' : 'a'" :href="type == 'link' && href" class="px-6 py-2 text-sm font-semibold bg-sky-500 text-white rounded-md border-2 border-sky-300">
        <slot></slot>
    </component>
</template>