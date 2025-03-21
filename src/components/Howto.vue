<script setup lang="ts">
import { ref } from "vue";

const isPlaying = ref(false);

const cards = [
  {
    image: new URL('/public/icons/Howto/Card-1.svg', import.meta.url).href,
    title: "Unduh Aplikasi PLN Mobile",
    description: "Tersedia di Google Play & App Store. Masuk dan daftarkan diri di PLN Mobile."
  },
  {
    image: new URL('/public/icons/Howto/Card-2.svg', import.meta.url).href,
    title: "Pilih Sambung Baru LSP Plus",
    description: "Isi data form Pasang Baru sesuai dengan permohonan Anda."
  },
  {
    image: new URL('/public/icons/Howto/Card-3.svg', import.meta.url).href,
    title: "Teknisi Datang ke Lokasi Anda",
    description: "Teknisi bersertifikat siap membantu dengan layanan terbaik."
  }
];

</script>

<template>
  <section class="w-full mx-auto py-12 px-6 justify-center">
    <!-- Header Section -->
    <div class="text-center">
      <section class="relative flex justify-center items-center py-10 px-4">
  <!-- Large Background Text -->
  <h1 class="absolute text-[40px] sm:text-[80px] md:text-[70px] lg:text-[100px] font-bold text-[#EDEFF5] opacity-50 leading-none">
    Sambung Baru LSP Plus
  </h1>

  <!-- Foreground Icon and Text -->
  <div class="relative flex items-center gap-2 sm:gap-4">
    <img src="/public/icons/About/IconLISTRIQU.svg" alt="Tentang Icon" width="24" height="30" class="sm:w-7 sm:h-9 md:w-8 md:h-10" />
    <h2 class="text-[#0B74BE] text-[24px] sm:text-[32px] md:text-[36px] font-bold">Sambung Baru LSP Plus</h2>
  </div>
</section>
      <p class="text-[#004F87] text-[24px] font-semibold mt-2">
        <span class="font-medium">Pesan Layanan</span>
        <span class="text-[#004F87] font-semibold">Sambung Baru LSP Plus <br /></span>
        <span class="font-medium">dalam 3 Langkah Mudah!</span>
      </p>
      <p class="text-[#696F8C] text-[16px] mt-4 max-w-4xl text-center mx-auto">
        <span class="font-bold">Sambung Baru LSP Plus</span> adalah layanan resmi dari PLN Mobile yang menghadirkan solusi kelistrikan
        profesional untuk rumah dan bisnis Anda. Yang di khususkan bagi pelanggan yang ingin melakukan pemasangan baru.
        Kami hadir dengan tenaga kerja bersertifikat, harga transparan, dan pelayanan yang cepat.
      </p>
    </div>

    <section class="container mx-auto py-12 px-4">
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 md:gap-x-10 md:gap-y-12 justify-center">
      
      <div v-for="(card, index) in cards" :key="index" 
           class="relative bg-white rounded-3xl border-2 border-[#EDEFF5] shadow-lg p-6 text-center w-full max-w-xs sm:max-w-sm md:max-w-md lg:max-w-lg mx-auto min-h-[300px] flex flex-col justify-end pb-10">
        
        <!-- Floating Image -->
        <div class="absolute -top-10 left-1/2 transform -translate-x-1/2 w-3/4 h-auto flex justify-center">
          <img :src="card.image" alt="Card Image" class="w-full h-auto object-cover" />
        </div>

        <!-- Card Content -->
        <div class="flex flex-row items-top gap-4 mt-32 text-left"> 
          <span class="w-10 h-10 flex items-center justify-center bg-[#0B74BE] text-white font-bold rounded-full text-lg">
            {{ index + 1 }}
          </span>
          
          <div class="flex flex-col">
            <h3 class="text-[#0B74BE] font-bold text-lg">{{ card.title }}</h3>
            <p class="text-[#696F8C] text-sm">{{ card.description }}</p>
          </div>
        </div>
      </div>

    </div>
  </section>



    <!-- Video Section -->
    <div class="relative w-full max-w-7xl mx-auto mt-12">
      <h3 class="text-[#696F8C] text-center font-medium text-[16px] my-2">Simak video tutorial dibawah ini:</h3>
      <div v-if="!isPlaying" class="relative">
        <img src="/public/icons/Howto/BgVideo.svg" alt="Video Thumbnail" class="w-full rounded-lg shadow-lg" />
        <button @click="isPlaying = true" class="absolute inset-0 flex items-center justify-center transition-transform duration-300 hover:scale-110">
          <img src="/public/icons/Howto/IconButtonPlay.svg" alt="Play" width="120" height="120" />
        </button>
      </div>

      <!-- YouTube Embed (Visible when clicked) -->
      <iframe
        v-if="isPlaying"
        class="w-full my-4 max-w-7xl h-[562px] rounded-lg shadow-lg"
        src="https://www.youtube.com/embed/gtJ63ZEtM4Y?autoplay=1"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        referrerpolicy="strict-origin-when-cross-origin"
        allowfullscreen
      ></iframe>
    </div>
  </section>
</template>

<style scoped>
/* Optional: Additional Styling */
</style>
