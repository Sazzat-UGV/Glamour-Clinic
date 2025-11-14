<script setup>
import { Icon } from '@iconify/vue';
import { ref } from 'vue'
const services = ref([
    {
        value: 'botox',
        label: 'Botox Treatments'
    },
    {
        value: 'fillers',
        label: 'Dermal Fillers'
    },
    {
        value: 'Laser',
        label: 'Laser Therapy'
    },
    {
        value: 'Facelift',
        label: 'Non-Surgical Facelift'
    },
    {
        value: 'Other',
        label: 'Other'
    },
])

const contactItems = ref([
    {
        icon: 'fa-solid:map-marker-alt',
        title: 'Our Location',
        content: '<p>123 Beauty Avenue, Medical District <br /> Casablanca 11564, Morocco</p>'
    },
    {
        icon: 'fa-solid:phone-alt',
        title: 'Phone Numbers',
        content: `<p>Appointments: <a href='tel:+1235566223' class='hover:text-pink-600'>+1235566223</a> <br />Emergency: <a href='tel:+1235566223' class='hover:txt-pink-600'>+1235566223</a></p>`
    },
    {
        icon: 'fa-solid:envelope',
        title: 'Email',
        content: `<p>Appointments: <a href='mailto:info@gmail.com' class='hover:text-pink-600'>mailto:info@gmail.com</a> <br /><a href='mailto:info@gmail.com' class='hover:txt-pink-600'>mailto:info@gmail.com</a></p>`
    },
    {
        icon: 'fa-solid:clock',
        title: 'Working Hours',
        content: `<p>Sunday -Thursday: 9:00 AM - 8:00 PM <br/>
            Friday: 2:00 AM - 9:00 PM <br/>
            Saturday:Closed
            </p>`
    },
])
</script>
<template>
    <section class="py-20 overflow-hidden bg-gradient-to-r from-pink-100 to-purple-100" id="specialists">
        <div class="container mx-auto px-4">
            <!-- Section Header -->
            <header class="text-center mb-16 relative" data-aos="fade-up" data-aos-delay="400">
                <span
                    class="absolute -top-10 left-1/2 transform -translate-x-1/2 w-20 h-20 rounded-full bg-pink-100 opacity-30 z-0"
                    aria-hidden="true"></span>
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4 relative z-10">
                    Contact<span class="text-pink-600">Our Clinic</span></h2>
                <p class="text-lg text-gray-600 max-w-2xl mx-auto relative z-10">
                    Reach out to schedule tour consultation or ask questions about our services
                </p>
                <span class="absolute -bottom-6 right-1/4 w-16 h-16 rounded-full bg-purple-100 opacity-20 z-0"
                    aria-hidden="true"></span>
            </header>
            <!-- Main Content -->
            <main class="flex flex-col lg:flex-row gap-12">
                <!-- Contact Info -->
                <aside class="lg:w-2/5">
                    <section class="bg-white rounded-2xl shadow-xl p-8 h-full">
                        <h2 class="text-2xl font-bold text-gray-800 mb-6">Get In Touch</h2>
                        <address class="space-y-6">
                            <article v-for="(item, index) in contactItems" :key="index" class="flex items-start">
                                <figure class="bg-pink-100 rounded-full p-3 mr-4 flex-shrink-0">
                                    <Icon :icon="item.icon" class="text-pink-600 text-xl" />
                                </figure>
                                <div>
                                    <h3 class="font-semibold text-gray-800 mb-1">
                                        {{ item.title }}
                                    </h3>
                                    <div class="text-gray-600" v-html="item.content"></div>
                                </div>
                            </article>
                        </address>
                        <figure class="mt-8 rounded-xl overflow-hidden shadow-md">
                            <img src="../assets/contactImg.png" alt="Glomour Clinic Building"
                                class="w-full h-48 object-cover hover:scale-105 transition-transform duration-500"
                                width="400" height="200" loading="lazy">
                        </figure>
                    </section>
                </aside>
                <!-- Contact Form -->
                <section class="lg:w-3/5">
                    <div class="bg-white rounded-2xl shadow-xl p-8 h-full">
                        <h2 class="text-2xl font-bold text-gray-800 mb-6">Send Us a Message</h2>
                        <form action="" class="space-y-6">
                            <fieldset class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                <div>
                                    <label for="name" class="block text-gray-700 font-medium mb-2">Full Name</label>
                                    <input type="text" name="name" id="name"
                                        class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border-transparent"
                                        placeholder="Your name" required>
                                </div>
                                <div>
                                    <label for="phone" class="block text-gray-700 font-medium mb-2">Phone Number</label>
                                    <input type="tel" name="phone" id="phone"
                                        class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border-transparent"
                                        placeholder="+1235566223" required>
                                </div>
                                <div>
                                    <label for="email" class="block text-gray-700 font-medium mb-2">Email
                                        Address</label>
                                    <input type="email" name="email" id="email"
                                        class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border-transparent"
                                        placeholder="example@gmail.com" required>
                                </div>
                                <div>
                                    <label for="service" class="block text-gray-700 font-medium mb-2">Service Interested
                                        In</label>
                                    <select name="service" id="service"
                                        class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border-transparent"
                                        placeholder="example@gmail.com" required>
                                        <option value="">Select a service</option>
                                        <option v-for="s in services" :value="s.value" :key="s.value">{{ s.label }}
                                        </option>
                                    </select>
                                </div>
                            </fieldset>
                                <div class="w-full">
                                    <label for="message" class="block text-gray-700 font-medium mb-2">Your
                                        Message</label>
                                    <textarea name="message" id="message" rows="5"
                                        class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-pink-500 focus:border-transparent"
                                        placeholder="Tell us about your concerns or question" required>
                                    </textarea>
                                </div>
                               <div class="text-center">
                                <button class="bg-pink-600 hover:bg-pink-700 text-white px-8 py-3 rounded-full transition shadow-lg w-full md:w-auto" aria-label="Submit contact form">Send Message</button>
                               </div>
                        </form>
                    </div>
                </section>
            </main>

            <!-- Google Map -->
            <figure class="mt-16 bg-white rounded-2xl shadow-xl overflow-hidden">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d34644.34959539246!2d90.3548777103424!3d23.79096523717392!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755c734c7c43a49%3A0xc015d831a1def368!2sShewrapara!5e1!3m2!1sen!2sbd!4v1763106843625!5m2!1sen!2sbd" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </figure>
        </div>
    </section>
</template>
<style scoped></style>
