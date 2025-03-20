<script setup lang="ts">
import { ref } from "vue";

// Data Testimoni
const allTestimonials = ref([
  {
    name: "Mila McSabbu",
    role: "Freelance Designer",
    image: "/src/assets/icons/Testimoni/User1.svg",
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore.",
  },
  {
    name: "Robert Fox",
    role: "Freelance Designer",
    image: "/src/assets/icons/Testimoni/User2.svg",
    text: "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
  },
  {
    name: "Jenny Wilson",
    role: "Freelance Designer",
    image: "/src/assets/icons/Testimoni/User3.svg",
    text: "Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
  },
  {
    name: "David Anderson",
    role: "Product Manager",
    image: "/src/assets/icons/Testimoni/User1.svg",
    text: "I had a fantastic experience with ListriQu! Their team was very professional and efficient.",
  },
  {
    name: "Emily Roberts",
    role: "Software Engineer",
    image: "/src/assets/icons/Testimoni/User2.svg",
    text: "ListriQu made my home feel safe with their excellent electrical service. Highly recommend them!",
  },
  {
    name: "John Doe",
    role: "Business Owner",
    image: "/src/assets/icons/Testimoni/User3.svg",
    text: "Top-notch service! Quick response and skilled technicians made my experience seamless.",
  },
]);

const visibleTestimonials = ref(allTestimonials.value.slice(0, 3)); // Menampilkan 3 data pertama
let startIndex = 0;

// Fungsi Next Testimoni
const nextTestimonials = () => {
  startIndex = (startIndex + 3) % allTestimonials.value.length;
  visibleTestimonials.value = allTestimonials.value.slice(startIndex, startIndex + 3);
};

// Fungsi Previous Testimoni
const prevTestimonials = () => {
  startIndex = (startIndex - 3 + allTestimonials.value.length) % allTestimonials.value.length;
  visibleTestimonials.value = allTestimonials.value.slice(startIndex, startIndex + 3);
};
</script>

<template>
  <section class="bg-[#004F87] py-12 w-full">
    <div class="container mx-auto bg-[url('/src/assets/icons/Testimoni/BgTestimoni.svg')] bg-no-repeat bg-auto bg-right-top">
      <!-- Badge -->
      <span class="bg-[#0075E3] text-white text-[16px] font-semibold px-4 py-2 rounded-full inline-block">
        TESTIMONI PELANGGAN
      </span>
      <div class="flex items-center justify-between">
        <!-- Title -->
        <h2 class="text-[#FBA919] text-[24px] md:text-[28px] font-semibold mt-4">
          Apa Kata Mereka Tentang ListriQu?
        </h2>
        <div class="flex gap-2">
          <button @click="prevTestimonials"
            class="w-10 h-10 rounded-full bg-[#B0C4DE] flex items-center text-center justify-center hover:bg-[#94B2D4] transition">
            <img src="/src/assets/icons/Testimoni/ButtonLeft.svg" alt="Left Arrow">
          </button>
          <button @click="nextTestimonials"
            class="w-10 h-10 rounded-full bg-[#FAB700] flex items-center text-center justify-center hover:bg-[#E5A500] transition">
            <img src="/src/assets/icons/Testimoni/ButtonRight.svg" alt="Right Arrow">
          </button>
        </div>
      </div>

      <!-- Testimonial Cards -->
      <div class="flex flex-col md:flex-row justify-center gap-6 mt-8">
        <div v-for="(testimonial, index) in visibleTestimonials" :key="index"
          class="bg-white p-6 rounded-lg shadow-lg max-w-sm text-left flex-1">
          <div class="flex items-center gap-3">
            <img :src="testimonial.image" alt="User" class="w-12 h-12 rounded-full object-cover" />
            <div>
              <h3 class="text-[#004F87] font-bold text-[16px]">{{ testimonial.name }}</h3>
              <p class="text-[#696F8C] text-[14px]">{{ testimonial.role }}</p>
            </div>
          </div>
          <p class="text-[#696F8C] mt-4 text-[14px] leading-relaxed">{{ testimonial.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
