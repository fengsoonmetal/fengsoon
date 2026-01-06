<template>
  <div>
    <Hero-Carousel />
    <div class="py-10"></div>

    <Hero-Services />
    <div class="py-10"></div>

    <Process />
    <Testimonials />
  </div>
</template>

<script setup>
import HeroCarousel from '@/components/Hero-Carousel.vue'
import HeroServices from '@/components/Hero-Services.vue'
import Process from '@/components/Process.vue'
import Testimonials from '@/components/Testimonials.vue'
</script>
