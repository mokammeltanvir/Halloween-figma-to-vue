<template>
  <section id="home" class="grid place-items-center mt-20 md:mt-10 overflow-hidden">

  <div class="grid grid-flow-row-dense grid-cols-1 lg:grid-cols-2 items-end gap-10 lg:gap-16 w-full px-0 lg:px-10">
  <div class="text-5xl md:text-6xl text-center md:text-left font-bold text-white w-full pb-20 order-2 lg:order-1">
  <div class="flex items-center gap-3 ml-24 md:ml-0">
  <h2 class="uppercase text-center md:text-left">Booo</h2>
  <img src="../assets/img/head1-img.png" alt="head1-img">
  </div>
  <h2 class="text-4xl md:text-5xl uppercase">Trick or Treat</h2>
  <p class="pt-5 text-lg font-normal ">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Enim commodi nostrum assumenda in sed impedit eum dolorum nam voluptatem soluta!</p>
    </div>

    <div class="w-full h-full md:pb-20 order-1 lg:order-2">
                <HomeSwiperVue />
            </div>            
  </div>


  <div class="grid place-items-center gap-2 text-white font-medium pt-8">
                <svg class="w-5 md:w-6" viewBox="0 0 26 49" fill="none" xmlns="http://www.w3.org/2000/svg"><rect x="1" y="1" width="24" height="47" rx="12" stroke="white" stroke-width="2"/>
                    <circle cx="13" cy="11" r="5" fill="#FF693A"/>
                </svg>
                Scroll
        </div>

  </section>
</template>
<script setup>
import HomeSwiperVue from './HomeSwiper.vue';
</script>