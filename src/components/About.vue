<script setup lang="ts">
</script>

<template>
  <section class="container mx-auto flex flex-col lg:flex-row items-center gap-10 py-12">
    <div class="container mx-auto h-auto justify-center">
      <section class="relative flex justify-center items-center py-10 px-4">
  <!-- Large Background Text -->
  <h1 class="absolute text-[60px] sm:text-[80px] md:text-[120px] font-bold text-[#EDEFF5] opacity-50 leading-none">
    TENTANG
  </h1>

  <!-- Foreground Icon and Text -->
  <div class="relative flex items-center gap-2 sm:gap-4">
    <img src="/src/assets/icons/About/IconLISTRIQU.svg" alt="Tentang Icon" width="24" height="30" class="sm:w-7 sm:h-9 md:w-8 md:h-10" />
    <h2 class="text-[#0B74BE] text-[28px] sm:text-[32px] md:text-[36px] font-bold">Tentang</h2>
  </div>
</section>

      <section class="flex flex-col lg:flex-row my-30 gap-4 ">
        <!-- Left Content -->
        <div class="lg:w-1/2 space-y-5">
          <span class="bg-[#004F87] text-white text-[16px] font-semibold px-4 py-2 rounded-full inline-block">
            OUR VALUES
          </span>
          <h2 class="text-[#004F87] text-[24px] font-semibold">Listrik Aman, Rumah Nyaman!</h2>
          <p class="text-[#696F8C] text-[16px] text-normal">
            <strong>ListriQu</strong> adalah layanan resmi dari PLN Mobile yang menghadirkan solusi kelistrikan 
            profesional untuk rumah dan bisnis Anda. Dari perbaikan instalasi hingga pemasangan baru, kami hadir dengan 
            tenaga kerja bersertifikat, harga transparan, dan pelayanan yang cepat.
          </p>

          <!-- Feature List -->
          <div class="space-y-4">
            <div class="flex items-center gap-3">
              <div class="bg-[#E9F6FF] rounded-full w-12 h-12 flex items-center justify-center">
                <img src="/src/assets/icons/About/IconCustomers.svg" alt="Customers" class="w-6 h-6 object-contain" />
              </div>
              <span class="text-[#004F87] font-semibold text-[18px]">100.000+ pelanggan puas</span>
            </div>

            <div class="flex items-center gap-3">
              <div class="bg-[#E9F6FF] rounded-full w-12 h-12 flex items-center justify-center">
                <img src="/src/assets/icons/About/IconCertifiedTechnician.svg" alt="Technician" class="w-6 h-6 object-contain" />
              </div>
              <span class="text-[#004F87] font-semibold text-[18px]">Teknisi Profesional & Bersertifikat</span>
            </div>

            <div class="flex items-center gap-3">
              <div class="bg-[#E9F6FF] rounded-full w-12 h-12 flex items-center justify-center">
                <img src="/src/assets/icons/About/IconFastService.svg" alt="Fast Service" class="w-6 h-6 object-contain" />
              </div>
              <span class="text-[#004F87] font-semibold text-[18px]">Layanan Cepat & Harga Transparan</span>
            </div>
          </div>
        </div>

<!-- Right Images -->
<div class="lg:w-1/2 lg:leftt-20 flex md:right-20 relative px-4">

<!-- Background Circle (Cream) -->
<div class="absolute top-10 right-14 sm:-top-20 lg:left-80 w-32 h-32 sm:w-56 sm:h-56 md:top-10 bg-[#FFF7E6] rounded-full z-0"></div>

<div class="relative w-2/3 top-15 right-2 md:-right-15 sm:w-[350px]  md:w-[400px] z-10 lg:left-8">
  <!-- Main Circular Image (Front) -->
  <img 
    src="/src/assets/Icons/About/BgTechnicianMain.svg" 
    alt="Technician"
    class="rounded-full w-full h-full object-cover border-4 border-white shadow-lg relative z-30" 
  />

  <!-- Technician Second (Bottom Right) -->
  <div class="absolute bottom-[-10%] sm:bottom-[-20px] right-[-40%] sm:right-[-200px] border-4 border-white rounded-full shadow-md z-20">
    <img 
      src="/src/assets/Icons/About/BgTechnicianWorking.svg" 
      alt="Technician Working"
      class="w-40 h-40 sm:w-[292px] sm:h-[292px] rounded-full object-cover" 
    />
  </div>

  <!-- PLN Mobile Logo (Top Right, Behind Technician Second) -->
  <div class="absolute -top-12 sm:-top-20 -right-10 sm:-right-20 rounded-full shadow-md z-10">
    <img 
      src="/src/assets/Icons/About/BgPlnMobile.svg" 
      alt="PLN Mobile"
      class="w-16 h-16 sm:w-[122px] sm:h-[122px] rounded-full object-cover" 
    />
  </div>

</div>

</div>

      </section>
    </div>
  </section>
</template>

<style scoped>
</style>
