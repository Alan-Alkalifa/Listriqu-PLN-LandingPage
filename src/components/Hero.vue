<script setup lang="ts">
const features = [
  { icon: new URL('/public/icons/Hero/IconCustomers.svg', import.meta.url).href, title: "Area Layanan Nasional" },
  { icon: new URL('/public/icons/Hero/IconCertifiedTechnician.svg', import.meta.url).href, title: "Penanganan 24 Jam" },
  { icon: new URL('/public/icons/Hero/IconFastService.svg', import.meta.url).href, title: "Layanan Konsultasi" },
  { icon: new URL('/public/icons/Hero/IconTechnicians.svg', import.meta.url).href, title: "Teknisi Bersertifikat" },
];


const stats = [
  { value: "200.000+", title: "Work Order" },
  { value: "Rp100B+", title: "Transaction" },
  { value: "400+", title: "Service Area" },
  { value: "4.8 (23K+)", title: "Customer Rating" },
];
</script><template>
  <!-- Hero Section with Background -->
   <div class="bg-[url('/public/icons/Hero/BgHero.svg')] bg-no-repeat bg-center bg-cover">
  <section
    class="container mx-auto flex flex-col lg:flex-row items-center xl:mt-52 lg:mt-40 lg:mb-1 mt-40 gap-10 py-12"
  >
    <!-- Left Content -->
    <div class="lg:w-full space-y-5 text-center lg:text-left">
      <h1 class="text-[#0B74BE] text-[32px] md:text-[40px] lg:text-[48px] font-semibold leading-tight">
        Layanan Total Permasalahan Listrik di Rumah Anda
      </h1>
      <p class="text-[#696F8C] text-[16px] md:text-[18px] lg:text-[20px]">
        <strong class="">ListriQu</strong> melayani kebutuhan instalasi dengan harga yang transparan dan kecepatan layanan yang prima.
      </p>

      <!-- Features -->
      <div class="flex flex-wrap justify-center lg:justify-start gap-6">
        <div v-for="feature in features" :key="feature.title" class="flex flex-col items-center text-center">
          <div class="rounded-full w-full h-full md:w-[100px] md:h-[100px] flex items-center justify-center">
            <img :src="feature.icon" :alt="feature.title" class="" />
          </div>
          <p class="mt-2 text-[12px] md:text-[14px] font-medium text-[#004F87]">{{ feature.title }}</p>
        </div>
      </div>

      <!-- Buttons -->
      <div class="flex gap-4 mt-6 md:mt-10 lg:mt-40 justify-center lg:justify-start">
        <!-- Primary Button -->
        <button
          class="px-6 md:px-9 py-3 bg-[#0B74BE] text-white rounded-full font-semibold shadow-lg flex items-center gap-2 hover:bg-[#094F7A] transition"
        >
          Daftar
          <span class="flex items-center justify-center w-6 h-6  border-2 border-[#0B74BE] text-[#0B74BE] rounded-full font-extrabold"><img src="/public/icons/Hero/ButtonRight1.svg"></span>
        </button>

        <!-- Outline Button -->
        <button
          class="group px-6 md:px-9 py-3 bg-white text-[#0B74BE] rounded-full font-semibold shadow-lg border-2 border-[#0B74BE] flex items-center gap-2 hover:bg-[#0B74BE] hover:text-white transition"
        >
          Detail
          <span class="flex items-center justify-center w-6 h-6">
    <img 
      src="/public/icons/Hero/ButtonRight2.svg" 
      class="group-hover:hidden"
    >
    <img 
      src="/public/icons/Hero/ButtonRight1.svg" 
      class="hidden group-hover:block"
    >
  </span>
        </button>
      </div>

      <p class="text-xs text-[#0B74BE] italic mt-10">*Mendaftar untuk melakukan pemesanan layanan ListrikQu home care.</p>
    </div>

    <!-- Right Images -->
    <div class="lg:w-1/2 lg:right-33 flex justify-center lg:right-10 mx-auto mt-10 md:mt-16 relative">
      <!-- Small Image with Blue Circle -->
      <div
        class="absolute -top-6 right-2 md:-top-12 md:-right-12 lg:-top-20 lg:-right-10 w-[100px] md:w-[140px] lg:w-[160px] h-[100px] md:h-[140px] lg:h-[160px] rounded-full border-[6px] md:border-[8px] border-[#0B74BE] overflow-hidden"
      >
        <img src="/public/icons/Hero/BgSecondary.svg" alt="Technician" class="w-full h-auto object-cover" />
      </div>

      <div
        class="relative w-[90%] md:w-[350px] lg:w-[400px] max-w-full h-auto rounded-full border-[8px] md:border-[12px] lg:border-[10px] border-white overflow-hidden"
      >
        <img src="/public/icons/Hero/BgMain.svg" alt="Technicians" class="fill-[#0B74BE] w-full rounded-full border-[18px] border-[#FAB700] h-auto object-cover" />
      </div>

      <!-- Light Bulb Icon -->
      <div class="absolute -top-20 right-14 md:-top-32 md:right-8 lg:-top-40 lg:right-12">
        <img src="/public/icons/Hero/BgLight.svg" alt="Light Bulb" class="w-20 md:w-28 lg:w-32 h-auto" />
      </div>
    </div>
  </section>

  <!-- Stats Section -->
  <section class="bg-[#0B74BE] w-full py-8">
    <div class="container flex flex-wrap lg:flex-nowrap justify-center lg:justify-between text-center gap-6 lg:gap-x-8">
      <div v-for="stat in stats" :key="stat.title" class="w-1/2 md:w-1/4 lg:w-auto min-w-[120px] p-4">
        <h1 class="text-[#FAB700] text-[32px] md:text-[36px] lg:text-[40px] font-bold">{{ stat.value }}</h1>
        <h2 class="text-[#81CBFF] text-[14px] md:text-[16px] lg:text-[18px] font-medium">{{ stat.title }}</h2>
      </div>
    </div>
  </section>
</div>
</template>


<style scoped>
/* Ensure body padding so navbar doesn't cover content */
body {
  padding-top: 100px; /* Adjust based on navbar height */
}
</style>
