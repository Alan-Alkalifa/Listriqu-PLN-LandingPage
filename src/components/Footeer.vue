<script setup lang="ts">
</script>

<template>
  <footer class="bg-[#0B74BE] border-t-8 border-[#FFC107] text-white py-12">
    <div class="container mx-auto px-6 flex flex-wrap justify-between my-10">
      <img src="/src/assets/icons/Footer/IconLogo.svg" alt="Logo">
    </div>

    <div class="container mx-auto items-center px-6 grid grid-cols-1 md:grid-cols-2 gap-8">
      <!-- Sections -->
      <div class="grid grid-cols-2 md:grid-cols-3 gap-8">
        <div>
          <h3 class="font-bold text-[13px] uppercase mb-3">Perusahaan</h3>
          <ul class="space-y-2 text-[14px] text-white/80">
            <li><a href="#">Beranda</a></li>
            <li><a href="#">Benefits</a></li>
            <li><a href="#">Team</a></li>
            <li><a href="#">Mitra</a></li>
          </ul>
        </div>

        <div>
          <h3 class="font-bold text-[13px] uppercase mb-3">Bantuan</h3>
          <ul class="space-y-2 text-[14px] text-white/80">
            <li><a href="#">F.A.Q</a></li>
            <li><a href="#">Contact Us</a></li>
            <li><a href="#">Terms & Conditions</a></li>
            <li><a href="#">Privacy Policy</a></li>
          </ul>
        </div>

        <div>
          <h3 class="font-bold text-[13px] uppercase mb-3">Product</h3>
          <ul class="space-y-2 text-[14px] text-white/80">
            <li><a href="#">ListriQu</a></li>
            <li><a href="#">Sambung LSP+</a></li>
            <li><a href="#">IML</a></li>
            <li><a href="#">PLN Mobile</a></li>
          </ul>
        </div>
      </div>

      <!-- Newsletter & Contact -->
      <div class="space-y-6">
        <div>
          <h3 class="font-bold text-[13px] uppercase">Subscribe to Newsletter</h3>
          <div class="mt-2 flex">
            <input type="email" placeholder="Enter email address"
              class=" w-full rounded-l-md bg-white text-black placeholder-[#8F95B2] p-4">
            <button class="bg-[#FFC107] w-1/2 text-[#0B74BE] px-4 py-2 rounded-r-md text-[16px] font-bold ">Join</button>
          </div>
        </div>
        <div class="flex flex-col md:flex-row md:justify-between space-y-4 md:space-y-0">
          <div>
            <h3 class="font-bold text-[13px] uppercase">Call Us</h3>
            <p class="text-[#FFC107] text-[20px] font-bold">08123 0000 572</p>
          </div>
          <div>
            <h3 class="font-bold text-[13px] uppercase">Email Us</h3>
            <p class="text-[#FFC107] text-[20px] font-bold">listriqu@iconpln.co.id</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Bar -->
    <div class="border-t border-white mt-8 pt-4 flex flex-col md:flex-row items-center justify-between text-sm text-white/80 px-6 max-w-6xl mx-auto">
      <p class="text-normal text-[14px]">© Copyright 2025, All Rights Reserved</p>
      <div class="flex gap-4 mt-4 md:mt-0">
        <a href="#"><img src="/src/assets/Icons/Footer/twitter.svg" alt="Twitter" class="w-5 h-5"></a>
        <a href="#"><img src="/src/assets/Icons/Footer/facebook.svg" alt="Facebook" class="w-5 h-5"></a>
        <a href="#"><img src="/src/assets/Icons/Footer/instagram.svg" alt="Instagram" class="w-5 h-5"></a>
        <a href="#"><img src="/src/assets/Icons/Footer/github.svg" alt="Github" class="w-5 h-5"></a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
</style>
