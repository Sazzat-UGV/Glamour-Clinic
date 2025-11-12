<script setup>
import { ref } from 'vue';

const stats = ref([
    { value: '2500+', label: 'Happy Clients' },
    { value: '15+', label: 'Specialists' },
    { value: '50+', label: 'Treatments' },
    { value: '10+', label: 'Years of Experience' },
]);
</script>

<template>
    <header id="home"
        class="relative overflow-hidden bg-gradient-to-r from-pink-50 to-purple-100 dark:from-pink-100 dark:to-purple-200">
        <article
            class="max-w-screen-xl mx-auto px-4 sm:px-8 py-16 md:py-24 flex flex-col-reverse lg:flex-row items-center gap-10">
            <!-- Text Section -->
            <section class="w-full lg:w-1/2 text-center lg:text-left">
                <hgroup data-aos="fade-up" data-aos-delay="200">
                    <h1
                        class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-800 mb-4 leading-tight">
                        Enhance Your Natural
                        <mark class="text-pink-600 bg-transparent">Beauty</mark>
                    </h1>
                    <p class="text-base sm:text-lg text-gray-600 mb-8 max-w-xl mx-auto lg:mx-0 leading-relaxed">
                        Discover advanced treatments designed to bring out your best self. Our
                        specialists ensure safety, comfort, and natural results every time.
                    </p>
                </hgroup>

                <!-- CTA Buttons -->
                <nav data-aos="fade-up" data-aos-delay="400"
                    class="flex flex-col sm:flex-row justify-center lg:justify-start gap-4 mb-10">
                    <a href="#appointment"
                        class="bg-pink-600 hover:bg-pink-700 text-white text-center px-8 py-3 rounded-full transition shadow-lg">
                        Book a Consultation
                    </a>
                    <a href="#services"
                        class="border border-pink-600 text-pink-600 hover:bg-pink-50 text-center px-8 py-3 rounded-full transition">
                        Explore Services
                    </a>
                </nav>

                <!-- Stats -->
                <aside data-aos="fade-up" data-aos-delay="600" class="py-4">
                    <ul class="flex flex-wrap justify-center lg:justify-start gap-x-8 gap-y-4 text-center">
                        <li v-for="(stat, index) in stats" :key="index" class="w-1/2 sm:w-auto">
                            <strong class="text-2xl sm:text-3xl font-bold text-pink-600 block">
                                {{ stat.value }}
                            </strong>
                            <small class="text-sm sm:text-base text-gray-600">{{
                                stat.label
                                }}</small>
                        </li>
                    </ul>
                </aside>
            </section>

            <!-- Image Section -->
            <figure data-aos="fade-up" data-aos-delay="700" class="w-full lg:w-1/2 flex justify-center relative">
                <div class="relative w-full max-w-xs sm:max-w-sm md:max-w-md">
                    <span
                        class="bg-pink-500 rounded-full w-64 g-64 sm:w-80 sm:h-80 absolute -top-10 -left-10 opacity-20"
                        aria-hidden="true"></span>
                    <span
                        class="bg-purple-400 rounded-full w-48 g-48 sm:w-64 sm:h-64 absolute -bottom-10 -right-10 opacity-20"
                        aria-hidden="true"></span>
                    <img src="../assets/hero.png" class="relative z-10 rounded-full shadow-2xl w-full object-cover"
                        width="400" height="400" loading="eager" alt="" />
                </div>
            </figure>
        </article>
    </header>
</template>

<style scoped></style>
