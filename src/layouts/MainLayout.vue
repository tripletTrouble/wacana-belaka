<script setup>
import Header from '../components/Header.vue';
import Footer from '../components/Footer.vue';

</script>

<template>
    <div class="min-h-screen flex flex-col justify-between">
        <Header></Header>
        <slot class="grow"></slot>

        <Footer></Footer>
    </div>
</template>