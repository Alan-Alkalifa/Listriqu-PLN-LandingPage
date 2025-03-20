<script setup lang="ts">
const services = [
  {
    icon: '/src/assets/Icons/Services/IconInstalasiListrik.svg',
    title: 'Instalasi Listrik',
    description: 'Pemasangan listrik baru di rumah atau bisnis Anda',
  },
  {
    icon: '/src/assets/Icons/Services/IconPerbaikanListrik.svg',
    title: 'Perbaikan Listrik',
    description: 'Solusi cepat untuk gangguan listrik',
  },
  {
    icon: '/src/assets/Icons/Services/IconPemeriksaan.svg',
    title: 'Pemeriksaan & Konsultasi',
    description: 'Cek keamanan dan efisiensi listrik di rumah',
  },
  {
    icon: '/src/assets/Icons/Services/IconBilling.svg',
    title: 'Billing & Pembayaran',
    description: 'Kemudahan pembayaran tagihan listrik',
  },
  {
    icon: '/src/assets/Icons/Services/IconTambahDaya.svg',
    title: 'Tambah Daya',
    description: 'Upgrade daya listrik sesuai kebutuhan Anda',
  },
];
</script>

<template>
  <div class="bg-[#F2F7FD]">
  <section class="container mx-auto py-12 px-6 text-center">
    <section class="relative flex justify-center items-center py-10 px-4">
  <!-- Large Background Text -->
  <h1 class="absolute text-[60px] sm:text-[80px] md:text-[80px] font-bold text-[#EDEFF5] opacity-50 leading-none">
    LAYANAN KAMI
  </h1>

  <!-- Foreground Icon and Text -->
  <div class="relative flex items-center gap-2 sm:gap-4">
    <img src="/src/assets/icons/About/IconLISTRIQU.svg" alt="LAYANAN KAMI Icon" width="24" height="30" class="sm:w-7 sm:h-9 md:w-8 md:h-10" />
    <h2 class="text-[#0B74BE] text-[28px] sm:text-[32px] md:text-[36px] font-bold">Layanan Kami</h2>
  </div>
</section>


    <!-- Service Grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-5  gap-10 mt-10">
      <div 
        v-for="(service, index) in services" 
        :key="index" 
        class="flex flex-col items-center justify-center text-center space-y-3"
      >
      <div class="h-full items-center">
        <img :src="service.icon" :alt="service.title" class="w-[208px] h-[176px] mb-2" />
        <h3 class="text-[20px] font-bold text-[#0B74BE]">{{ service.title }}</h3>
        <p class="text-[12px] text-[#8F95B2] max-w-[200px]">{{ service.description }}</p>
      </div>
      <div class="">
        <button 
          class="mt-4 px-6 py-2 border-2 border-[#0B74BE] text-[#0B74BE] rounded-full flex items-center gap-2 hover:bg-[#0B74BE] hover:text-white transition"
        >
          <span class="text-[16px] font-semibold">Detail Layanan →</span>
        </button>
      </div>
      </div>
    </div>
 </section>
</div>
</template>

<style scoped>
/* Additional styling can be added here */
</style>
