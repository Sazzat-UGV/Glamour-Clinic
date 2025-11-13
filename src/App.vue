<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css'
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Service from './components/Service.vue';
onMounted(() => {
  AOS.init();
})
</script>
<template>
  <Header />
  <Hero />
  <Service />
</template>
<style scoped></style>
