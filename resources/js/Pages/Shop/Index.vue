<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Head } from '@inertiajs/vue3';
import VehicleCard from '@/Components/Vehicle/VehicleCard.vue';

const imgCar = 'https://as1.ftcdn.net/jpg/10/22/24/80/220_F_1022248039_7LDxHRi3Mlt9BK3wzLBUGZp9XAO1gt2s.jpg';

const categories = ['Todos', 'SUV', 'Compacto', 'Deportivo', 'Familiar', 'Eléctrico'];
const vehicles = [
    { id: 1, marca: 'Toyota', model: 'Corolla', any: 2022, preu: 22490, km: 25000, image: imgCar },
    { id: 2, marca: 'BMW', model: 'Serie 3', any: 2021, preu: 35990, km: 42000, image: imgCar },
    { id: 3, marca: 'Volkswagen', model: 'Golf', any: 2023, preu: 26990, km: 12000, image: imgCar },
    { id: 4, marca: 'Mercedes', model: 'Classe A', any: 2020, preu: 29990, km: 55000, image: imgCar },
    { id: 5, marca: 'Audi', model: 'A4', any: 2022, preu: 38990, km: 30000, image: imgCar },
    { id: 6, marca: 'Seat', model: 'León', any: 2023, preu: 21990, km: 15000, image: imgCar },
];
</script>

<template>
    <AppLayout>
        <Head title="Catálogo - ReCarStore" />

        <section class="bg-black py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <h1 class="text-3xl font-bold mb-4">Catálogo</h1>
                <p class="text-gray-400">Encuentra el coche perfecto</p>
            </div>
        </section>

        <section class="bg-gray-900 py-4 px-4">
            <div class="max-w-7xl mx-auto flex flex-wrap gap-2">
                <button v-for="cat in categories" :key="cat" class="px-3 py-1 text-sm border border-gray-700">
                    {{ cat }}
                </button>
            </div>
        </section>

        <section class="bg-black py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
                    <VehicleCard v-for="v in vehicles" :key="v.id" :vehicle="v" />
                </div>
            </div>
        </section>
    </AppLayout>
</template>