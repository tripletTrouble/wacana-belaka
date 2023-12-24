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
    <component :is="type !== 'link' ? 'button' : 'a'" :href="type == 'link' ? href : null" class="px-6 py-2 text-sm font-semibold text-gray-600 rounded-md border-2 border-gray-400 bg-gray-100">
        <slot></slot>
    </component>
</template>