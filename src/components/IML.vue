<script setup lang="ts">
import { ref } from 'vue';

const steps = ref([
  {
    image: '/src/assets/icons/IMS/Step-1.svg',
    title: 'Pilih instalatir',
    description: 'Pilih instalatir yang kompeten dan memiliki sertifikat akreditasi.'
  },
  {
    image: '/src/assets/icons/IMS/Step-2.svg',
    title: 'Pasang IML',
    description: 'Pasang IML sesuai dengan standar teknis kelistrikan.'
  },
  {
    image: '/src/assets/icons/IMS/Step-3.svg',
    title: 'Ajukan Permohonan SLO',
    description: 'Ajukan permohonan Sertifikat Laik Operasi (SLO) ke LIT yang ditunjuk pemerintah.'
  },
  {
    image: '/src/assets/icons/IMS/Step-4.svg',
    title: 'Ajukan Permohonan ke PLN',
    description: 'Setelah SLO diterbitkan, ajukan permohonan penyambungan ke PLN.'
  }
]);
</script>

<template>
  <section class="w-full mx-auto py-12 px-6 justify-center">
    <!-- Header Section -->
    <div class="text-center">
      <section class="relative flex justify-center items-center py-10 px-4">
  <!-- Large Background Text -->
  <h1 class="absolute text-[40px] sm:text-[80px] md:text-[70px] lg:text-[100px] font-bold text-[#EDEFF5] opacity-50 leading-none">
    Instalasi Milik Langganan
  </h1>

  <!-- Foreground Icon and Text -->
  <div class="relative flex items-center gap-2 sm:gap-4">
    <img src="/src/assets/icons/About/IconLISTRIQU.svg" alt="Tentang Icon" width="24" height="30" class="sm:w-7 sm:h-9 md:w-8 md:h-10" />
    <h2 class="text-[#0B74BE] text-[24px] sm:text-[32px] md:text-[36px] font-bold">Instalasi Milik Langganan (IML)</h2>
  </div>
</section>
      <p class="text-[#004F87] text-[24px] font-semibold mt-2">
        <span class="font-medium">Apa yang di maksud dengan IML?</span>
      </p>
      <p class="text-[#696F8C] text-[16px] mt-4 max-w-4xl text-center mx-auto">
        <span class="font-bold">Instalasi Milik Langganan (IML) </span> adalah instalasi listrik di dalam bangunan milik pelanggan, seperti kabel, panel, saklar, stop kontak, dan fitting lampu, yang harus memenuhi persyaratan teknis dan memiliki Sertifikat Laik Operasi (SLO) sebelum dapat dihubungkan ke jaringan PLN. Baca selengkapnya.
      </p>

      <p class="text-[#004F87] text-[24px] font-semibold mt-2">
        4 Langkah Proses Pemasangan IML:
      </p>
    </div>

    <section class="w-full mx-auto py-12 px-6 justify-center">
    <div class="text-center">
      <h2 class="text-[#0B74BE] text-[24px] sm:text-[32px] md:text-[36px] font-bold">4 Langkah Proses Pemasangan IML</h2>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 mt-10">
      <div v-for="(step, index) in steps" :key="index" class="bg-white shadow-lg rounded-2xl p-6 border border-gray-200 flex flex-col ">
        <img :src="step.image" alt="Step Image" class=" mb-4" />
        <div class="flex text-left gap-2">
        <span class="text-[#0B74BE] font-bold text-lg">{{ index + 1 }}.</span>
        <h3 class="text-[#0B74BE] font-bold text-lg">{{ step.title }}</h3>
    </div>
        <p class="text-[#696F8C] text-sm mt-2">{{ step.description }}</p>
      </div>
    </div>
  </section>

  </section>
</template>

<style scoped>
</style>
