  <script setup>
import { onMounted, ref } from "vue";

const navbar = ref('');
const showMenu = ref(false);

onMounted(() => {
  window.onscroll = () => {
  if(window.scrollY === 0) {
    navbar.value.classList.remove('bg-primary-200')
  } else {
    navbar.value.classList.add('bg-primary-200')
  }
}
})
</script>
<template>
  <!-- Navbar -->
  <nav ref="navbar" class="fixed top-0 left-0 w-full bg-primary-200 z-20 transition duration-200">
  <div class="container flex items-center justify-between h-20">
  <div class="relative z-30 flex items-center gap-2 mb-2 lg:mb-0">
  <a href="/" class="flex">
    <h1 class="text-white font-bold tex-lg lg:text-2xl mr-2">Hallow<span class="text-secondary">ee</span>nd</h1>
    <img src="../assets/img/logo/Vector.svg" alt="" srcset="">
    </a>
  </div>

  <div class="flex items-center gap-2 lg:hidden">    
    <button class="relative z-30 px-4 py-2 bg-secondary text-white transition hover:bg-orange-600 rounded-full font-medium text-sm uppercase w-full lg:w-auto -mt-1.5">Donate</button>
    <!-- toggle menu -->
    <button class="relative z-30 px-4 py-2 transition rounded-full font-medium text-sm uppercase w-full lg:w-auto -mt-1.5" @click="showMenu = !showMenu">
          <img src="../assets/mobilemenu.svg" alt="">
    </button>
    </div>
    <div
        class="
          absolute lg:static top-20 inset-x-0
          flex flex-col lg:flex-row items-center gap-5 lg:gap-10
          bg-primary-200 lg:bg-transparent pt-5 pb-10 px-5 lg:p-0
          transition duration-500 lg:duration-200 lg:-translate-y-0
        "
        :class="!showMenu ? 'translate-y-[-150%]' : '-translate-y-0'"
      >
        <a @click="showMenu = false" class="text-white font-medium transition hover:text-secondary" href="#home">Home</a>
        <a @click="showMenu = false" class="text-white font-medium transition hover:text-secondary" href="#category">Category</a>
        <a @click="showMenu = false" class="text-white font-medium transition hover:text-secondary" href="#about">About</a>
        <a @click="showMenu = false" class="text-white font-medium transition hover:text-secondary" href="#trick-or-treat">Trick or Treat</a>
        <button class="hidden md:block px-8 py-3 rounded-full text-white font-medium tracking-wider uppercase bg-secondary transition hover:bg-orange-600 w-full lg:w-auto">Donate</button>
      </div>
  
  </div>
    
  </nav>
  </template>
