<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css'
onMounted(()=>{
  AOS.init();
})
</script>
<template>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>

</template>
<style scoped>

</style>
