<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <AppLayout>
        <Head title="Qui Som - ReCarStore" />

        <section class="bg-black text-white py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h1 class="text-4xl lg:text-5xl font-bold mb-4">Qui Som</h1>
                <p class="text-gray-500 text-lg">Més de 10 anys d'excel·lència</p>
            </div>
        </section>

        <section class="bg-gray-950 py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid lg:grid-cols-2 gap-16 items-center">
                    <div>
                        <h2 class="text-3xl font-bold text-white mb-6">La nostra història</h2>
                        <p class="text-gray-400 mb-6">
                            ReCarStore neix l'any 2015 amb la vocació de transformar la manera en què la gent compra cotxes de segona mà. 
                            La nostra missió és oferir vehicles de qualitat amb total transparència i confiança.
                        </p>
                        <p class="text-gray-400 mb-6">
                            Amb més de 500 vehicles venuts i una taxa de satisfacció del 98%, ens hem consolidat com un dels 
                            referents del sector a Catalunya.
                        </p>
                        <p class="text-gray-400">
                            Tots els nostres cotxes passen un estricte control de qualitat de més de 100 punts abans 
                            de sortir a la venda, garantint la teva tranquil·litat.
                        </p>
                    </div>
                    <div>
                        <img src="https://images.unsplash.com/photo-1560179707-f14e90ef3623?w=600" alt="Oficines ReCarStore" class="rounded-xl border border-gray-800">
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-black py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl font-bold text-white mb-12 text-center">Els nostres valors</h2>
                <div class="grid md:grid-cols-3 gap-8">
                    <div class="text-center">
                        <div class="w-16 h-16 bg-gray-900 rounded-full flex items-center justify-center mx-auto mb-4 border border-gray-800">
                            <svg class="h-8 w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-white mb-2">Qualitat</h3>
                        <p class="text-gray-500">Tots els nostres vehicles passen controls exhaustius.</p>
                    </div>
                    <div class="text-center">
                        <div class="w-16 h-16 bg-gray-900 rounded-full flex items-center justify-center mx-auto mb-4 border border-gray-800">
                            <svg class="h-8 w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-white mb-2">Confiança</h3>
                        <p class="text-gray-500">Transparència total en tot el procés.</p>
                    </div>
                    <div class="text-center">
                        <div class="w-16 h-16 bg-gray-900 rounded-full flex items-center justify-center mx-auto mb-4 border border-gray-800">
                            <svg class="h-8 w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-white mb-2">Servei</h3>
                        <p class="text-gray-500">Assistència personalitzada.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gray-950 py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h2 class="text-3xl font-bold text-white mb-6">Video Presentació</h2>
                <div class="max-w-3xl mx-auto">
                    <div class="bg-gray-900 rounded-xl aspect-video flex items-center justify-center border border-gray-800">
                        <div class="text-center text-gray-500">
                            <svg class="h-16 w-16 mx-auto mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            <p>Video de presentació de ReCarStore</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </AppLayout>
</template>
