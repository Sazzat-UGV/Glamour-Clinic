<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css'
import Header from './components/Header.vue';
onMounted(() => {
  AOS.init();
})
</script>
<template>
  <Header />
</template>
<style scoped></style>
