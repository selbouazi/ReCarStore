<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Head } from '@inertiajs/vue3';

const contactInfo = {
    address: 'C/ Gran Via, 123',
    city: '08014 Barcelona',
    phone: '+34 93 123 45 67',
    email: 'info@recarstore.cat',
    hours: 'Dilluns - Divendres: 9:00 - 20:00'
};
</script>

<template>
    <AppLayout>
        <Head title="Contacte - ReCarStore" />

        <section class="bg-black text-white py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h1 class="text-4xl lg:text-5xl font-bold mb-4">Contacte</h1>
                <p class="text-gray-500 text-lg">Estem aquí per ajudar-te</p>
            </div>
        </section>

        <section class="bg-gray-950 py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid lg:grid-cols-2 gap-16">
                    <div>
                        <h2 class="text-2xl font-bold text-white mb-6">Envia'ns un missatge</h2>
                        <form class="space-y-6">
                            <div class="grid md:grid-cols-2 gap-4">
                                <div>
                                    <label class="block text-sm font-medium text-gray-400 mb-2">Nom</label>
                                    <input type="text" class="w-full bg-gray-900 border border-gray-800 text-white px-4 py-3 rounded-lg focus:border-gray-600 focus:outline-none transition">
                                </div>
                                <div>
                                    <label class="block text-sm font-medium text-gray-400 mb-2">Cognoms</label>
                                    <input type="text" class="w-full bg-gray-900 border border-gray-800 text-white px-4 py-3 rounded-lg focus:border-gray-600 focus:outline-none transition">
                                </div>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">Email</label>
                                <input type="email" class="w-full bg-gray-900 border border-gray-800 text-white px-4 py-3 rounded-lg focus:border-gray-600 focus:outline-none transition">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">Assumpte</label>
                                <select class="w-full bg-gray-900 border border-gray-800 text-white px-4 py-3 rounded-lg focus:border-gray-600 focus:outline-none transition">
                                    <option>Consulta general</option>
                                    <option>Volem vendre un cotxe</option>
                                    <option>Finançament</option>
                                    <option>Garantia</option>
                                    <option>Altres</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">Missatge</label>
                                <textarea rows="5" class="w-full bg-gray-900 border border-gray-800 text-white px-4 py-3 rounded-lg focus:border-gray-600 focus:outline-none transition" placeholder="Escriu el teu missatge..."></textarea>
                            </div>
                            <button type="submit" class="w-full bg-white text-black py-3 rounded-lg font-semibold hover:bg-gray-100 transition">
                                Enviar missatge
                            </button>
                        </form>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-white mb-6">Informació de contacte</h2>
                        <div class="bg-gray-900 rounded-xl p-6 border border-gray-800 space-y-6">
                            <div class="flex items-start space-x-4">
                                <div class="w-12 h-12 bg-black rounded-lg flex items-center justify-center shrink-0">
                                    <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                                    </svg>
                                </div>
                                <div>
                                    <h3 class="font-semibold text-white">Adreça</h3>
                                    <p class="text-gray-500">{{ contactInfo.address }}</p>
                                    <p class="text-gray-500">{{ contactInfo.city }}</p>
                                </div>
                            </div>
                            <div class="flex items-start space-x-4">
                                <div class="w-12 h-12 bg-black rounded-lg flex items-center justify-center shrink-0">
                                    <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                                    </svg>
                                </div>
                                <div>
                                    <h3 class="font-semibold text-white">Telèfon</h3>
                                    <p class="text-gray-500">{{ contactInfo.phone }}</p>
                                </div>
                            </div>
                            <div class="flex items-start space-x-4">
                                <div class="w-12 h-12 bg-black rounded-lg flex items-center justify-center shrink-0">
                                    <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                                    </svg>
                                </div>
                                <div>
                                    <h3 class="font-semibold text-white">Email</h3>
                                    <p class="text-gray-500">{{ contactInfo.email }}</p>
                                </div>
                            </div>
                            <div class="flex items-start space-x-4">
                                <div class="w-12 h-12 bg-black rounded-lg flex items-center justify-center shrink-0">
                                    <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                                    </svg>
                                </div>
                                <div>
                                    <h3 class="font-semibold text-white">Horari</h3>
                                    <p class="text-gray-500">{{ contactInfo.hours }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </AppLayout>
</template>
