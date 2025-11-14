<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css'
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Service from './components/Service.vue';
import About from './components/About.vue';
import Specialists from './components/Specialists.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
onMounted(() => {
  AOS.init();
})
</script>
<template>
  <Header />
  <Hero />
  <Service />
  <About />
  <Specialists />
  <Contact />
  <Footer />
</template>
<style scoped></style>
