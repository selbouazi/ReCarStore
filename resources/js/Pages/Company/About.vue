<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Head } from '@inertiajs/vue3';

const imgCar = 'https://as1.ftconvert.net/jpg/10/22/24/80/220_F_1022248039_7LDxHRi3Mlt9BK3wzLBUGZp9XAO1gt2s.jpg';
</script>

<template>
    <AppLayout>
        <Head title="Quiénes Somos - ReCarStore" />

        <section class="bg-black py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <h1 class="text-3xl font-bold mb-4">Quiénes Somos</h1>
                <p class="text-gray-400">Más de 10 años de excelencia</p>
            </div>
        </section>

        <section class="bg-gray-900 py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <div class="grid md:grid-cols-2 gap-8">
                    <div>
                        <h2 class="text-2xl font-bold mb-4">Nuestra Historia</h2>
                        <p class="text-gray-400 mb-4">
                            ReCarStore nació en 2015 con el objetivo de transformar la forma en que la gente compra coches de segunda mano.
                            Nuestra misión es ofrecer vehículos de calidad con total transparencia y confianza.
                        </p>
                        <p class="text-gray-400 mb-4">
                            Con más de 500 vehículos vendidos y una tasa de satisfacción del 98%, nos hemos consolidado como un referente del sector.
                        </p>
                        <p class="text-gray-400">
                            Todos nuestros coches pasan un estricto control de calidad.
                        </p>
                    </div>
                    <div>
                        <img :src="imgCar" alt="ReCarStore" class="w-full rounded">
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-black py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <h2 class="text-2xl font-bold mb-8 text-center">Nuestros Valores</h2>
                <div class="grid md:grid-cols-3 gap-8">
                    <div class="text-center">
                        <h3 class="text-xl font-bold mb-2">Calidad</h3>
                        <p class="text-gray-400">Todos nuestros vehículos pasan controles exhaustivos.</p>
                    </div>
                    <div class="text-center">
                        <h3 class="text-xl font-bold mb-2">Confianza</h3>
                        <p class="text-gray-400">Transparencia total en todo el proceso.</p>
                    </div>
                    <div class="text-center">
                        <h3 class="text-xl font-bold mb-2">Servicio</h3>
                        <p class="text-gray-400">Asistencia personalizada.</p>
                    </div>
                </div>
            </div>
        </section>
    </AppLayout>
</template>