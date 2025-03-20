<script setup lang="ts">
import { ref } from "vue";

const isDropdownOpen = ref(false);
const isMenuOpen = ref(false);
const selectedLanguage = ref("ID");

const selectLanguage = (lang: string) => {
  selectedLanguage.value = lang;
  isDropdownOpen.value = false;
};
</script>

<template>
  <header class="fixed top-0 left-0 w-full bg-white shadow-md z-50">
    <!-- Top Navbar -->
    <section class="bg-[#004F87] w-full">
  <nav class="container mx-auto flex flex-col md:flex-row items-center justify-center md:justify-between text-white text-sm py-2 px-4">
    
    <!-- Emergency Contact (Tetap di atas di layar kecil) -->
    <div class="flex items-center gap-2 text-center md:text-left mb-2 md:mb-0">
      <img src="/src/assets/icons/Navbar/IconEmergencyCall1.svg" alt="Emergency" width="20" height="20" />
      <a class="font-normal" href="#">Emergency: <span class="font-semibold">Contact Center PLN 123</span></a>
    </div>

    <!-- Contact Info (Responsive) -->
    <div class="flex flex-wrap justify-center md:justify-end items-center gap-4 md:gap-6 text-center">
      
      <!-- Email -->
      <div class="flex items-center gap-2">
        <img src="/src/assets/icons/Navbar/IconMail.svg" alt="Mail" width="20" height="20" />
        <a class="font-medium" href="mailto:listriqu@iconpln.co.id">listriqu@iconpln.co.id</a>
      </div>

      <!-- Separator (Hidden di Mobile) -->
      <span class="text-[#FFD700] hidden md:inline">|</span>

      <!-- Phone Number -->
      <div class="flex items-center gap-2">
        <img src="/src/assets/icons/Navbar/IconPhoneCall.svg" alt="Phone Call" width="20" height="20" />
        <a class="font-medium" href="tel:081230000572">08123 0000 572</a>
      </div>

      <!-- Separator (Hidden di Mobile) -->
      <span class="text-[#FFD700] hidden md:inline">|</span>

      <!-- 24-Hour Call Center -->
      <div class="flex items-center gap-2">
        <img src="/src/assets/icons/Navbar/IconClock.svg" alt="24 Hour Service" width="20" height="20" />
        <a class="font-medium" href="#">Call Center 24 Jam</a>
      </div>

    </div>
  </nav>
</section>



    <!-- Main Navbar -->
    <section class="border-b-2 border-[#EDEFF5] w-full">
      <nav class="container mx-auto flex justify-between items-center h-16 px-4">
        <a href="#" class="flex-shrink-0">
          <img src="/src/assets/icons/Navbar/LogoListriqu.svg" alt="Listriqu Logo" width="145" height="40" />
        </a>

        <!-- Mobile Menu Button -->
        <button class="md:hidden text-[#0B74BE]" @click="isMenuOpen = !isMenuOpen">
          <img src="/src/assets/icons/Navbar/IconMenu.svg" alt="Menu" width="32" height="32" />
        </button>

        <!-- Desktop Menu -->
        <ul class="hidden md:flex text-[#8F95B2] text-base gap-6">
          <li><a href="#" class="hover:text-[#0B74BE] hover:border-b-2 hover:border-[#0B74BE] font-medium">Beranda</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] hover:border-b-2 hover:border-[#0B74BE] font-medium">Tentang</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] hover:border-b-2 hover:border-[#0B74BE] font-medium">Layanan</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] hover:border-b-2 hover:border-[#0B74BE] font-medium">LSP+</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] hover:border-b-2 hover:border-[#0B74BE] font-medium">Testimoni</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] hover:border-b-2 hover:border-[#0B74BE] font-medium">Bantuan</a></li>
        </ul>

        <!-- Language Selector -->
        <div class="relative hidden md:block">
          <button class="hidden items-center gap-2" @click="isDropdownOpen = !isDropdownOpen">
            <img src="/src/assets/icons/Navbar/IconLanguage.svg" alt="Language" width="24" height="24" />
            <span class="text-[#696F8C]">{{ selectedLanguage }}</span>
            <img src="/src/assets/icons/Navbar/IconDropdown.svg" alt="Dropdown" width="16" height="16" />
          </button>
          <ul v-if="isDropdownOpen" class="absolute right-0 mt-2 bg-white text-black shadow-lg rounded-md w-32 py-2">
            <li><a href="#" class="block px-4 py-2 hover:bg-gray-200" @click="selectLanguage('ID')">ID</a></li>
            <li><a href="#" class="block px-4 py-2 hover:bg-gray-200" @click="selectLanguage('EN')">EN</a></li>
          </ul>
        </div>
      </nav>

      <!-- Mobile Dropdown Menu -->
      <div v-if="isMenuOpen" class="md:hidden bg-white w-full shadow-lg">
        <ul class="text-[#8F95B2] text-base text-center py-4 space-y-4">
          <li><a href="#" class="hover:text-[#0B74BE] font-medium">Beranda</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] font-medium">Tentang</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] font-medium">Team</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] font-medium">LSP+</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] font-medium">Testimoni</a></li>
          <li><a href="#" class="hover:text-[#0B74BE] font-medium">Bantuan</a></li>
          <li class="hidden invisible">
            <button class="flex items-center justify-center gap-2 w-full text-[#696F8C]" @click="isDropdownOpen = !isDropdownOpen">
              <img src="/src/assets/icons/Navbar/IconLanguage.svg" alt="Language" width="24" height="24" />
              <span>{{ selectedLanguage }}</span>
              <img src="/src/assets/icons/Navbar/IconDropdown.svg" alt="Dropdown" width="16" height="16" />
            </button>
            <ul v-if="isDropdownOpen" class="mt-2 bg-white text-black shadow-lg rounded-md w-32 mx-auto py-2">
              <li><a href="#" class="block px-4 py-2 hover:bg-gray-200" @click="selectLanguage('ID')">ID</a></li>
              <li><a href="#" class="block px-4 py-2 hover:bg-gray-200" @click="selectLanguage('EN')">EN</a></li>
            </ul>
          </li>
        </ul>
      </div>
    </section>
  </header>
</template>
