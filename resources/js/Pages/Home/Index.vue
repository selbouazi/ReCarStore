<script setup>
import { Head, Link } from '@inertiajs/vue3';
import AppLayout from '@/Layouts/AppLayout.vue';
import VehicleCard from '@/Components/Vehicle/VehicleCard.vue';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
});

const imgCar = 'https://as1.ftcdn.net/jpg/10/22/24/80/220_F_1022248039_7LDxHRi3Mlt9BK3wzLBUGZp9XAO1gt2s.jpg';

const vehicles = [
    { id: 1, marca: 'Toyota', model: 'Corolla', any: 2022, km: 25000, preu: 22490, image: imgCar },
    { id: 2, marca: 'BMW', model: 'Serie 3', any: 2021, km: 42000, preu: 35990, image: imgCar },
    { id: 3, marca: 'Volkswagen', model: 'Golf', any: 2023, km: 12000, preu: 26990, image: imgCar },
    { id: 4, marca: 'Mercedes', model: 'Classe A', any: 2020, km: 55000, preu: 29990, image: imgCar }
];
</script>

<template>
    <AppLayout>
        <Head title="Inicio - ReCarStore" />

        <section class="bg-black py-16 px-4">
            <div class="max-w-7xl mx-auto">
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <div>
                        <h1 class="text-4xl font-bold mb-4">Tu coche de segunda mano</h1>
                        <p class="text-gray-400 mb-6">Coches de calidad con garantía</p>
                        <Link href="/shop" class="inline-block bg-white text-black px-6 py-2">Ver Catálogo</Link>
                    </div>
                    <div>
                        <img :src="imgCar" alt="Coche" class="w-full rounded">
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gray-900 py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <h2 class="text-2xl font-bold mb-8">Vehículos Destacados</h2>
                <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
                    <VehicleCard v-for="v in vehicles" :key="v.id" :vehicle="v" />
                </div>
                <div class="mt-8 text-center">
                    <Link href="/shop" class="text-white underline">Ver todos los vehículos</Link>
                </div>
            </div>
        </section>

        <section class="bg-black py-12 px-4">
            <div class="max-w-7xl mx-auto text-center">
                <h2 class="text-2xl font-bold mb-6">¿Quieres vender tu coche?</h2>
                <p class="text-gray-400 mb-6">Te ofrecemos la mejor valoración</p>
                <Link href="/contact" class="inline-block bg-white text-black px-6 py-2">Contacto</Link>
            </div>
        </section>
    </AppLayout>
</template>