<script setup lang="ts">
import { ref } from "vue";

// Data FAQ
const faqs = ref([
  { question: "Apa itu ListriQu?", answer: "ListriQu adalah layanan yang menyediakan berbagai solusi kelistrikan dengan teknisi profesional dan terpercaya.", isOpen: false },
  { question: "Bagaimana cara memesan layanan ListriQu?", answer: "Anda bisa memesan layanan ListriQu melalui aplikasi resmi kami atau menghubungi customer service.", isOpen: false },
  { question: "Apakah teknisi yang datang terpercaya?", answer: "Ya, semua teknisi kami telah melewati proses seleksi ketat dan memiliki sertifikasi resmi.", isOpen: false },
  { question: "Apakah ada biaya tambahan?", answer: "Biaya tambahan mungkin berlaku tergantung pada jenis layanan dan lokasi Anda.", isOpen: false },
  { question: "Apa itu Sambung Baru LSP+?", answer: "Sambung Baru LSP+ adalah layanan khusus untuk pemasangan listrik baru dengan prosedur cepat dan aman.", isOpen: false },
]);

// Fungsi Toggle FAQ
const toggleFAQ = (index: number) => {
  faqs.value[index].isOpen = !faqs.value[index].isOpen;
};
</script>

<template>
  <section class="py-12 w-full">
    <section class="relative flex justify-center items-center py-10 px-4">
      <!-- Large Background Text -->
      <h1 class="absolute text-[60px] sm:text-[80px] md:text-[80px] lg:text-[128px] font-bold text-[#EDEFF5] opacity-50 leading-none">
        F.A.Q
      </h1>

      <!-- Foreground Icon and Text -->
      <div class="relative flex items-center gap-2 sm:gap-4">
        <img src="/src/assets/icons/About/IconLISTRIQU.svg" alt="LAYANAN KAMI Icon" width="24" height="30" class="sm:w-7 sm:h-9 md:w-8 md:h-10" />
        <h2 class="text-[#0B74BE] text-[28px] sm:text-[32px] md:text-[36px] font-bold">Frequently Asked Questions</h2>
      </div>
    </section>
    <section class="flex container flex-col lg:flex-row my-5 gap-4 ">
        <!-- Left Content -->
        <div class="lg:w-1/2 space-y-5">
          <span class="bg-[#004F87] text-white text-[16px] font-semibold px-4 py-2 rounded-full inline-block">
            F.A.Q
          </span>
          <h2 class="text-[#004F87] text-[24px] font-semibold">Punya Pertanyaan? Kami Siap Membantu!</h2>
        </div>
        </section>
    
    
    <div class="container mx-auto px-4">
    <!-- Grid Layout for FAQ and Image -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
      <!-- FAQ List -->
      <div class="space-y-4">
        <div v-for="(faq, index) in faqs" :key="index">
          <button @click="toggleFAQ(index)" class="w-full text-left flex items-center justify-between px-6 py-4 bg-[#E9F6FF] text-[#004F87] font-normal text-[18px] rounded-full">
            {{ faq.question }}
            <span>
              <img v-if="faq.isOpen" src="/src/assets/icons/Faq/IconArrowUp.svg" alt="Collapse" />
              <img v-else src="/src/assets/icons/Faq/IconArrowDown.svg" alt="Expand" />
            </span>
          </button>
          <div v-if="faq.isOpen" class="px-6 py-2 text-[#696F8C] bg-white rounded-lg shadow-md">
            {{ faq.answer }}
          </div>
        </div>

        <!-- Lihat Semua FAQ -->
        <div class="text-center mt-6">
          <a href="#" class="text-[#0B74BE] font-medium text-[14px]">Lihat Semua FAQ</a>
        </div>
      </div>

      <!-- Image (Hidden on Mobile, Visible on Desktop) -->
      <div class="hidden lg:flex justify-center">
        <img src="/src/assets/icons/Faq/BgRight.svg" alt="FAQ Background Image" class="max-w-sm lg:max-w-md xl:max-w-lg">
      </div>
    </div>
  </div>
  </section>
</template>
