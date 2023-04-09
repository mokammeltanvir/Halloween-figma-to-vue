<script setup>
import {Pagination} from 'swiper';
 // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';
  import 'swiper/css/pagination';

  const modules = [Pagination];

  
</script>
<template>
  <swiper
  :modules="modules"
    :slides-per-view="1"
    :pagination="{ clickable: true }"
    class="pb-8"
  >
    <swiper-slide><img src="../assets/img/home1-img.webp" class="w-2/3 lg:w-[90%]" alt=""></swiper-slide>
    <swiper-slide><img src="../assets/img/slider_img1.webp" class="w-2/3 lg:w-[90%]" alt=""></swiper-slide>
    <swiper-slide><img src="../assets/img/slider_img2.webp" class="w-2/3 lg:w-[90%]" alt=""></swiper-slide>
    <swiper-slide><img src="../assets/img/slider_img3.webp" class="w-2/3 lg:w-[90%]" alt=""></swiper-slide>
    <swiper-slide><img src="../assets/img/slider_img4.webp" class="w-2/3 lg:w-[90%]" alt=""></swiper-slide>
  </swiper>
</template>

<style>
  .swiper-pagination-bullet {
    @apply w-3 h-3 bg-white opacity-100
  }
  .swiper-pagination-bullet.swiper-pagination-bullet-active {
    @apply rounded-xl w-6  bg-secondary
  }
</style>