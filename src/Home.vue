<script setup>
import MainLayout from "./layouts/MainLayout.vue";
import PrimaryButton from "./components/PrimaryButton.vue";
import SecondaryButton from "./components/SecondaryButton.vue";
import { onMounted } from "vue";

onMounted(() => {
  var messages = [
    "creativity",
    "imagination",
    "idea",
    "opinion",
    "productivity",
  ];
  var ix = 1;

  function changeMessage(index) {
    if (index == messages.length) {
      ix = -1;
      index = 0;
    }

    document.getElementById("message").innerText = messages[index];

    ix = ix + 1;
  }

  setInterval(() => {
    changeMessage(ix);
  }, 3000);
});
</script>

<template>
  <MainLayout>
    <div id="hero" class="relative">
      <img
        src="./assets/dragos-gontariu-54VAb3f1z6w-unsplash.jpg"
        alt="Creativity"
        class="object-cover w-screen h-screen transition"
        id="hero-image"
      />
      <div
        id="cta-wrapper"
        class="absolute inset-0 flex items-center justify-center flex-col"
      >
        <div
          class="bg-gray-100 bg-opacity-80 py-12 w-full md:w-[80%] lg:w-[70%] xl:w-[60%] rounded-lg"
        >
          <h1
            class="text-5xl lg:text-6xl font-extrabold text-sky-500 text-center"
          >
            WACANA
          </h1>
          <p class="text-sky-600 text-center lg:text-lg italic mb-6 md:mb-8">
            "The point that everything was started"
          </p>
          <p class="text-center italic lg:text-lg mb-6 md:mb-8">
            We are the place of
            <span class="font-bold" id="message">creativity</span>.
          </p>
          <p
            class="text-center px-6 xl:px-8 text-sm lg:text-lg leading-relaxed mb-6 md:mb-8"
          >
            Kami bermaksud untuk menjadi wadah bagi siapapun untuk berekspresi
            dan berwacana. Mari dukung kami dan jadilah bagian dari kami.
          </p>
          <div
            class="flex flex-col md:flex-row justify-center items-center gap-4 lg:gap-6"
          >
            <PrimaryButton :type="'link'" class="w-fit flex gap-2">
              <span>Beli Produk Kami</span>
            </PrimaryButton>
            <SecondaryButton :type="'link'" :href="'#jadi-kontributor'" class="w-fit flex gap-2">
              <span>Jadi Kontributor</span>
            </SecondaryButton>
          </div>
        </div>
      </div>
    </div>
    <div class="h-screen md:h-auto py-6 md:py-12 xl:py-24 flex items-center justify-center" title="Sekapur Sirih">
      <div class="p-4 w-[90%] md:w-[60%] xl:w-[50%] shadow-2xl border rounded-lg">
        <h2
          class="font-bold text-center font-2xl mx-auto w-fit px-4 border-b border-gray-600"
        >
          Sekapur Sirih
        </h2>
        <p class="mt-5 xl:mt-12 px-4 text-sm md:text-base leading-relaxed">
          <span class="font-semibold text-sky-500">Wacana Belaka</span>
          didedikasikan untuk menjadi sarana untuk berekspresi dan berwacana
          yang tanpa batas. Kamu bisa menulis opini, ide, gagasan, pendapat,
          pengalaman, atau bahkan memamerkan karya di sini.
        </p>
        <p class="px-4 text-sm md:text-base mt-5 xl:mt-8 leading-relaxed">
          Kami membutuhkan bantuan untuk tetap berdiri di sini. Dukung kami
          dengan menyebarluaskan karya kami melalui media sosial, komunitas,
          forum diskusi, atau apapun bentuknya, agar semakin banyak orang yang
          menikmati sarana ini. Jika kamu punya cukup uang, bantu kami dengan
          menggunakan jasa kami atau membeli produk kami. Jadilah bagian dari
          <span class="font-semibold text-sky-500">Wacana</span> dan mulailah
          ber<span class="font-semibold text-sky-500">Wacana</span> hari ini.
        </p>
        <p class="mt-8 xl:mt-10 text-sm md:text-base text-right px-4 leading-relaxed">
          Regards, <br />
          The Founders
        </p>
      </div>
    </div>
    <div id="jadi-kontributor" class="py-12 w-screen bg-gray-100">
      <h2 class="text-center font-bold text-xl text-sky-500">Bergabung dengan Kami</h2>
      <div class="mt-8 flex flex-col gap-6 px-4 md:w-[80%] lg:w-[70%] xl:w-[50%] mx-auto">
        <div class="border-2 border-sky-200 shadow-xl p-6 rounded-lg bg-white">
          <h3 class="font-semibold text-sky-500">Jadi Artisan</h3>
          <p class="mt-3 text-xs leading-relaxed md:text-sm lg:text-base">Artisan adalah pengrajin, mereka memiliki bakat dan keterampilan untuk membuat sesuatu. Kamu bisa memakai jasa artisan untuk membuat sesuatu. Bagi kamu yang punya bakat dan keterampilan bisa bergabung menjadi artisan. Mulailah menghasilkan bersama kami.</p>
          <div class="mt-5">
            <SecondaryButton :type="'link'" :href="'#'" class="text-xs md:text-base">
              Daftar jadi artisan
            </SecondaryButton>
          </div>
        </div>
        <div class="border-2 border-sky-200 shadow-xl p-6 rounded-lg bg-white">
          <h3 class="font-semibold text-sky-500">Jadi Blogger</h3>
          <p class="mt-3 text-xs leading-relaxed md:text-sm lg:text-base">Bagi kamu yang suka menulis tapi nggak tahu mulai dari mana, kamu bisa bergabung menjadi blogger di Wacana Belaka. Di sini kamu bisa nulis apapun, opini, pendapat, pengalaman, cerita liburan, keluh kesah, atau apapun yang menurutmu penting.</p>
          <div class="mt-5">
            <SecondaryButton :type="'link'" :href="'#'" class="text-xs md:text-base">
              Daftar jadi blogger
            </SecondaryButton>
          </div>
        </div>
      </div>
    </div>
    <div id="sponsors" class="py-16">
      <h2 class="text-xl text-center font-bold pb-2 border-b border-gray-700 px-6 w-fit mx-auto">Sponsor Kami</h2>
      <div class="flex flex-col gap-4 justify-center items-center mt-8">
        <p class="text-sm lg:text-base mb-3">Upps, ... kami belum punya sponsor</p>
        <SecondaryButton :type="'link'" :href="'#'" class="text-xs md:text-sm lg:text-base">Yuk, jadi yang pertama</SecondaryButton>
      </div>
    </div>
  </MainLayout>
</template>

<style scoped>
#hero-image {
  animation-duration: 0.5s;
  animation-name: fadeIn;
}

#cta-wrapper {
  animation-duration: 1s;
  animation-name: fade;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}

@keyframes fade {
  from {
    opacity: 0;
    margin-top: -50px;
  }

  to {
    opacity: 1;
    margin-top: 0px;
  }
}
</style>
