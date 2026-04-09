<script setup>
import { Head, Link } from '@inertiajs/vue3';
import AppLayout from '@/Layouts/AppLayout.vue';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
});

const featuredVehicles = [
    {
        id: 1,
        marca: 'Toyota',
        model: 'Corolla',
        any: 2022,
        quilometratge: 25000,
        preu: 22490,
        imatge: 'https://images.unsplash.com/photo-1623869675781-80aa31012a5a?w=600',
        certificat: 'Excel·lent'
    },
    {
        id: 2,
        marca: 'BMW',
        model: 'Serie 3',
        any: 2021,
        quilometratge: 42000,
        preu: 35990,
        imatge: 'https://images.unsplash.com/photo-1555215695-3004980ad54e?w=600',
        certificat: 'Molt Bé'
    },
    {
        id: 3,
        marca: 'Volkswagen',
        model: 'Golf',
        any: 2023,
        quilometratge: 12000,
        preu: 26990,
        imatge: 'https://images.unsplash.com/photo-1606611013016-969c19ba27bb?w=600',
        certificat: 'Excel·lent'
    },
    {
        id: 4,
        marca: 'Mercedes-Benz',
        model: 'Classe A',
        any: 2020,
        quilometratge: 55000,
        preu: 29990,
        imatge: 'https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?w=600',
        certificat: 'Bé'
    }
];

const news = [
    {
        id: 1,
        title: 'Nou inventari de vehicles híbrids',
        date: '15 Mar 2026',
        excerpt: 'Hem incorporat una àmplia gamma de cotxes híbrids certificats.',
        image: 'https://images.unsplash.com/photo-1593941707882-a5bba14938c7?w=400'
    },
    {
        id: 2,
        title: 'Black Friday: 15% de descompte',
        date: '10 Mar 2026',
        excerpt: 'Aquest cap de setmana, descomptes especials en tots els nostres vehicles.',
        image: 'https://images.unsplash.com/photo-1449965408869-eaa3f722e40d?w=400'
    }
];

const faqs = [
    {
        question: 'Els cotxes tenen garantia?',
        answer: 'Sí, tots els nostres vehicles inclouen 12 mesos de garantia mecànica.'
    },
    {
        question: 'Puc finançar la compra?',
        answer: 'Oferim finances amb condicions especials per als nostres clients.'
    },
    {
        question: 'Acceptem el meu cotxe com a part de pagament?',
        answer: 'Sí, acceptem el teu vehicle actual com a part de pagament.'
    }
];

const stats = [
    { number: '500+', label: 'Vehicles venuts' },
    { number: '98%', label: 'Clients satisfets' },
    { number: '10', label: 'Anys d\'experiència' },
    { number: '24h', label: 'Assistència' }
];
</script>

<template>
    <AppLayout>
        <Head title="Inici - ReCarStore" />

        <section class="relative bg-black text-white overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-br from-gray-900 via-gray-900 to-black"></div>
            <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-32 lg:py-40">
                <div class="grid lg:grid-cols-2 gap-16 items-center">
                    <div>
                        <img src="/img/recarsore_logo.png" alt="ReCarStore" class="h-20 w-auto mb-6">
                        <h1 class="text-5xl lg:text-7xl font-bold leading-tight mb-6">
                            El teu cotxe,
                            <span class="text-white">el teu estil</span>
                        </h1>
                        <p class="text-xl text-gray-400 mb-10 max-w-lg">
                            Més de 10 anys venent cotxes de qualitat amb les millors garanties del mercat.
                        </p>
                        <div class="flex flex-wrap gap-4">
                            <Link href="/cataleg" class="bg-white text-black px-8 py-4 font-semibold hover:bg-gray-100 transition flex items-center space-x-2">
                                <span>Veure Catàleg</span>
                            </Link>
                            <Link href="/qui-som" class="border border-gray-700 text-white px-8 py-4 font-semibold hover:bg-gray-900 transition">
                                Coneix-nos
                            </Link>
                        </div>
                    </div>
                    <div class="hidden lg:block">
                        <div class="relative">
                            <img src="https://images.unsplash.com/photo-1492144534655-ae79c964c9d7?w=800" alt="Cotxe" class="rounded-2xl">
                            <div class="absolute -bottom-4 -left-4 bg-white text-black px-4 py-2 rounded-lg">
                                <span class="text-sm font-semibold">+500 vehicles venuts</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gray-950 py-20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                    <div v-for="stat in stats" :key="stat.label" class="text-center">
                        <div class="text-4xl lg:text-5xl font-bold text-white">{{ stat.number }}</div>
                        <div class="text-gray-500 mt-2 text-sm uppercase tracking-wider">{{ stat.label }}</div>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-black py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-3xl lg:text-4xl font-bold text-white mb-4">Vehicles Destacats</h2>
                    <p class="text-gray-500 max-w-xl mx-auto">Descobreix la nostra selecció dels millors cotxes disponibles.</p>
                </div>

                <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                    <div v-for="vehicle in featuredVehicles" :key="vehicle.id" class="bg-gray-900 rounded-xl overflow-hidden hover:bg-gray-800 transition group border border-gray-800">
                        <div class="relative aspect-video overflow-hidden">
                            <img :src="vehicle.imatge" :alt="vehicle.marca + ' ' + vehicle.model" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
                            <span class="absolute top-3 left-3 bg-white text-black text-xs font-semibold px-2 py-1 rounded">
                                {{ vehicle.certificat }}
                            </span>
                        </div>
                        <div class="p-5">
                            <p class="text-xs text-gray-500 uppercase tracking-wider mb-1">{{ vehicle.marca }}</p>
                            <h3 class="text-lg font-semibold text-white mb-2">{{ vehicle.model }} {{ vehicle.any }}</h3>
                            <p class="text-sm text-gray-500 mb-4">{{ vehicle.quilometratge.toLocaleString() }} km</p>
                            <div class="flex items-center justify-between">
                                <span class="text-xl font-bold text-white">{{ vehicle.preu.toLocaleString() }}€</span>
                                <Link :href="`/vehicle/${vehicle.id}`" class="text-sm text-gray-400 hover:text-white transition">
                                    Veure →
                                </Link>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="text-center mt-12">
                    <Link href="/cataleg" class="inline-block border border-white text-white px-8 py-3 font-medium hover:bg-white hover:text-black transition">
                        Veure Tots els Vehicles
                    </Link>
                </div>
            </div>
        </section>

        <section class="bg-gray-900 py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid lg:grid-cols-2 gap-16 items-center">
                    <div>
                        <h2 class="text-3xl font-bold text-white mb-6">Vols vendre el teu cotxe?</h2>
                        <p class="text-gray-400 mb-8">
                            Acceptem el teu vehicle actual com a part de pagament. 
                            Els nostres experts t'oferiran la millor valoració del mercat.
                        </p>
                        <Link href="/contacte" class="inline-block bg-white text-black px-6 py-3 font-medium hover:bg-gray-100 transition">
                            Demana una valoració
                        </Link>
                    </div>
                    <div class="hidden lg:flex justify-center">
                        <div class="w-48 h-48 bg-gray-800 rounded-2xl flex items-center justify-center">
                            <svg class="h-20 w-20 text-gray-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M8 7h8m-8 5h8m-4 4v2m0 0h2a2 2 0 002-2v-4a2 2 0 00-2-2h-2l-3-4H7L4 7H2a2 2 0 00-2 2v4a2 2 0 002 2h2l3 4h2a2 2 0 002-2v-4a2 2 0 00-2-2z" />
                            </svg>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-black py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-3xl lg:text-4xl font-bold text-white mb-4">Notícies</h2>
                    <p class="text-gray-500">Les últimes novetats de ReCarStore.</p>
                </div>

                <div class="grid md:grid-cols-2 gap-8">
                    <div v-for="item in news" :key="item.id" class="bg-gray-900 rounded-xl overflow-hidden hover:bg-gray-800 transition border border-gray-800">
                        <img :src="item.image" :alt="item.title" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <p class="text-sm text-gray-500 mb-2">{{ item.date }}</p>
                            <h3 class="text-xl font-semibold text-white mb-2">{{ item.title }}</h3>
                            <p class="text-gray-400 mb-4">{{ item.excerpt }}</p>
                            <a href="#" class="text-gray-400 hover:text-white transition text-sm">Llegir més →</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gray-950 py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid lg:grid-cols-2 gap-16">
                    <div>
                        <h2 class="text-3xl font-bold text-white mb-8">Preguntes FreqÜents</h2>
                        <div class="space-y-4">
                            <div v-for="faq in faqs" :key="faq.question" class="bg-gray-900 rounded-lg p-6 border border-gray-800">
                                <h3 class="font-semibold text-white mb-2">{{ faq.question }}</h3>
                                <p class="text-gray-400">{{ faq.answer }}</p>
                            </div>
                        </div>
                        <Link href="/faq" class="inline-flex items-center space-x-2 mt-6 text-gray-400 hover:text-white transition">
                            <span>Veure totes les preguntes</span>
                            <span>→</span>
                        </Link>
                    </div>

                    <div>
                        <h2 class="text-3xl font-bold text-white mb-8">On Som</h2>
                        <div class="bg-gray-900 rounded-xl h-80 flex items-center justify-center border border-gray-800">
                            <div class="text-center text-gray-500">
                                <svg class="h-12 w-12 mx-auto mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                                </svg>
                                <p class="font-medium text-white">C/ Gran Via, 123</p>
                                <p>08014 Barcelona</p>
                                <p class="mt-4 text-sm">Dill-Div 9:00-20:00</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-black py-20 border-t border-gray-900">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h2 class="text-2xl font-bold text-white mb-4">Rep les nostres novetats</h2>
                <p class="text-gray-500 mb-8">Subscriu-te per rebre ofertes exclusives.</p>
                <form class="flex flex-col sm:flex-row gap-3 max-w-lg mx-auto">
                    <input type="email" placeholder="El teu email" class="flex-1 bg-gray-900 border border-gray-800 text-white px-4 py-3 rounded-lg focus:outline-none focus:border-gray-600 transition">
                    <button type="submit" class="bg-white text-black px-6 py-3 rounded-lg font-medium hover:bg-gray-100 transition">
                        Subscriu-te
                    </button>
                </form>
            </div>
        </section>
    </AppLayout>
</template>
