<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Head } from '@inertiajs/vue3';

const categories = ['Tots', 'SUV', 'Compacte', 'Esportiu', 'Familiar', 'Elèctric'];
const vehicles = [
    { id: 1, marca: 'Toyota', model: 'Corolla', any: 2022, preu: 22490, km: 25000, imatge: 'https://images.unsplash.com/photo-1623869675781-80aa31012a5a?w=600', certificat: 'Excel·lent' },
    { id: 2, marca: 'BMW', model: 'Serie 3', any: 2021, preu: 35990, km: 42000, imatge: 'https://images.unsplash.com/photo-1555215695-3004980ad54e?w=600', certificat: 'Molt Bé' },
    { id: 3, marca: 'Volkswagen', model: 'Golf', any: 2023, preu: 26990, km: 12000, imatge: 'https://images.unsplash.com/photo-1606611013016-969c19ba27bb?w=600', certificat: 'Excel·lent' },
    { id: 4, marca: 'Mercedes-Benz', model: 'Classe A', any: 2020, preu: 29990, km: 55000, imatge: 'https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?w=600', certificat: 'Bé' },
    { id: 5, marca: 'Audi', model: 'A4', any: 2022, preu: 38990, km: 30000, imatge: 'https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?w=600', certificat: 'Excel·lent' },
    { id: 6, marca: 'Seat', model: 'León', any: 2023, preu: 21990, km: 15000, imatge: 'https://images.unsplash.com/photo-1619682817481-e994891cd1f5?w=600', certificat: 'Molt Bé' },
];
</script>

<template>
    <AppLayout>
        <Head title="Catàleg - ReCarStore" />

        <section class="bg-black text-white py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h1 class="text-4xl lg:text-5xl font-bold mb-4">Catàleg</h1>
                <p class="text-gray-500 text-lg">Troba el cotxe perfecte per a tu</p>
            </div>
        </section>

        <section class="bg-gray-950 py-6 border-b border-gray-900">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex flex-wrap gap-3 items-center justify-between">
                    <div class="flex flex-wrap gap-2">
                        <button v-for="cat in categories" :key="cat" class="px-4 py-2 rounded-full text-sm font-medium transition"
                            :class="cat === 'Tots' ? 'bg-white text-black' : 'bg-gray-900 text-gray-400 hover:bg-gray-800 border border-gray-800'">
                            {{ cat }}
                        </button>
                    </div>
                    <select class="bg-gray-900 border border-gray-800 text-white px-4 py-2 rounded-lg text-sm focus:border-gray-600">
                        <option>Ordenar per</option>
                        <option>Preu: Menor a Major</option>
                        <option>Preu: Major a Menor</option>
                        <option>Any: Nou a Vell</option>
                    </select>
                </div>
            </div>
        </section>

        <section class="bg-black py-16">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div v-for="vehicle in vehicles" :key="vehicle.id" class="bg-gray-900 rounded-xl overflow-hidden hover:bg-gray-800 transition border border-gray-800">
                        <div class="relative aspect-video">
                            <img :src="vehicle.imatge" :alt="vehicle.marca + ' ' + vehicle.model" class="w-full h-full object-cover">
                            <span class="absolute top-3 left-3 bg-white text-black text-xs font-semibold px-2 py-1 rounded">
                                {{ vehicle.certificat }}
                            </span>
                        </div>
                        <div class="p-5">
                            <p class="text-xs text-gray-500 uppercase tracking-wider mb-1">{{ vehicle.marca }}</p>
                            <h3 class="text-lg font-semibold text-white mb-2">{{ vehicle.model }} {{ vehicle.any }}</h3>
                            <div class="flex justify-between text-sm text-gray-500 mb-4">
                                <span>{{ vehicle.km.toLocaleString() }} km</span>
                                <span>Gasolina</span>
                            </div>
                            <div class="flex items-center justify-between pt-4 border-t border-gray-800">
                                <span class="text-xl font-bold text-white">{{ vehicle.preu.toLocaleString() }}€</span>
                                <button class="bg-white text-black px-4 py-2 rounded-lg text-sm font-medium hover:bg-gray-100 transition">
                                    Veure detall
                                </button>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="mt-12 text-center">
                    <button class="border border-gray-700 text-white px-8 py-3 rounded-lg font-medium hover:bg-gray-900 transition">
                        Carregar més vehicles
                    </button>
                </div>
            </div>
        </section>
    </AppLayout>
</template>
