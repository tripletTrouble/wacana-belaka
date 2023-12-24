<script setup>
import { reactive } from "vue";
import MobileLink from "./MobileLink.vue";
import LargeMenu from "./LargeMenu.vue";

const state = reactive({
  isMobileMenuOpen: false,
});
</script>

<template>
  <header
    class="w-screen flex justify-center py-3 border-b-2 border-sky-400 bg-gray-100 fixed top-0 left-0 z-10"
  >
    <div id="header-content" class="w-[90vw] flex justify-between items-center">
      <div id="logo-wrapper" class="">
        <img
          src="../assets/wacana.png"
          alt="Logo Wacana Belaka"
          class="h-8 w-8"
        />
      </div>
      <div id="menu-lg" class="hidden md:flex gap-2 lg:gap-4">
        <LargeMenu :link="'#'" :text="'Tentang Wacana'"></LargeMenu>
        <LargeMenu :link="'#'" :text="'Artisan'"></LargeMenu>
        <LargeMenu :link="'#'" :text="'Blog'"></LargeMenu>
        <LargeMenu :link="'#'" :text="'Dukung Kami'"></LargeMenu>
      </div>
      <div
        id="mobile-menu"
        class="fixed top-14 mt-0.5 right-0 w-screen bg-gray-100 transition pb-4"
        :class="{ hidden: !state.isMobileMenuOpen }"
      >
        <MobileLink :link="'#'" :text="'Tentang Wacana'"></MobileLink>
        <MobileLink :link="'#'" :text="'Artisan'"></MobileLink>
        <MobileLink :link="'#'" :text="'Blog'"></MobileLink>
        <MobileLink :link="'#'" :text="'Dukung Kami'"></MobileLink>
        <p class="text-sky-500 text-center mt-5" style="font-size: 10px;">
          Crafted with
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            data-slot="icon"
            class="w-4 h-4 inline text-rose-400"
          >
            <path
              d="m11.645 20.91-.007-.003-.022-.012a15.247 15.247 0 0 1-.383-.218 25.18 25.18 0 0 1-4.244-3.17C4.688 15.36 2.25 12.174 2.25 8.25 2.25 5.322 4.714 3 7.688 3A5.5 5.5 0 0 1 12 5.052 5.5 5.5 0 0 1 16.313 3c2.973 0 5.437 2.322 5.437 5.25 0 3.925-2.438 7.111-4.739 9.256a25.175 25.175 0 0 1-4.244 3.17 15.247 15.247 0 0 1-.383.219l-.022.012-.007.004-.003.001a.752.752 0 0 1-.704 0l-.003-.001Z"
            />
          </svg>
          by <a class="underline hover:text-sky-300 font-semibold" target="_blank" href="https://github.com/tripletTrouble">tripletTrouble</a>
        </p>
      </div>
      <div id="mobile-menu-trigger" class="md:hidden">
        <button
          class="trasition"
          @click="state.isMobileMenuOpen = !state.isMobileMenuOpen"
        >
          <svg
            :class="{ hidden: state.isMobileMenuOpen }"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            data-slot="icon"
            class="w-6 h-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
            />
          </svg>

          <svg
            :class="{ hidden: !state.isMobileMenuOpen }"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            data-slot="icon"
            class="w-6 h-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M6 18 18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
    </div>
  </header>
</template>

<style scoped>
#mobile-menu {
  animation-duration: 0.5s;
  animation-name: fadeIn;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    right: -50px;
  }

  to {
    opacity: 1;
  }
}
</style>
