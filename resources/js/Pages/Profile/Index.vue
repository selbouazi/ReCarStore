<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Head, Link } from '@inertiajs/vue3';
</script>

<template>
    <AppLayout>
        <Head title="Perfil - ReCarStore" />

        <section class="bg-black py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <h1 class="text-3xl font-bold mb-4">Mi Perfil</h1>
                <p class="text-gray-400">Bienvenido, {{ $page.props.auth.user?.name }}!</p>
            </div>
        </section>

        <section class="bg-gray-900 py-12 px-4">
            <div class="max-w-7xl mx-auto">
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="bg-black p-6">
                        <h2 class="text-xl font-bold mb-4">Información de la Cuenta</h2>
                        <div class="space-y-4 text-gray-400">
                            <p><strong class="text-white">Nombre:</strong> {{ $page.props.auth.user?.name }}</p>
                            <p><strong class="text-white">Email:</strong> {{ $page.props.auth.user?.email }}</p>
                        </div>
                        <Link href="/account" class="inline-block mt-4 bg-white text-black px-4 py-2 text-sm">
                            Editar Perfil
                        </Link>
                    </div>

                    <div class="bg-black p-6">
                        <h2 class="text-xl font-bold mb-4">Mis Pedidos</h2>
                        <p class="text-gray-400">Sin pedidos todavía</p>
                        <Link href="/orders" class="inline-block mt-4 text-white underline text-sm">
                            Ver Historial de Pedidos
                        </Link>
                    </div>
                </div>
            </div>
        </section>
    </AppLayout>
</template>