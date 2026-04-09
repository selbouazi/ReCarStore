<script setup>
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3';

defineProps({
    cartCount: {
        type: Number,
        default: 0
    }
});

const showingMobileMenu = ref(false);
</script>

<template>
    <nav class="bg-gray-900 border-b border-gray-800 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4">
            <div class="flex justify-between h-14">
                <div class="flex items-center">
                    <Link href="/" class="flex items-center">
                        <img src="/img/recarsore_logo.png" alt="ReCarStore" class="h-10 w-auto">
                    </Link>
                </div>

                <div class="hidden md:flex items-center space-x-6">
                    <Link href="/" class="text-gray-300 hover:text-white">Inicio</Link>
                    <Link href="/shop" class="text-gray-300 hover:text-white">Catálogo</Link>
                    <Link href="/about" class="text-gray-300 hover:text-white">Quiénes Somos</Link>
                    <Link href="/contact" class="text-gray-300 hover:text-white">Contacto</Link>
                </div>

                <div class="flex items-center space-x-4">
                    <button class="p-2 text-gray-400 relative">
                        <svg class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                        </svg>
                        <span v-if="cartCount > 0" class="absolute -top-1 -right-1 bg-white text-black text-xs rounded-full h-4 w-4 flex items-center justify-center">{{ cartCount }}</span>
                    </button>

                    <template v-if="$page.props.auth.user">
                        <Link href="/profile" class="text-gray-300 text-sm">{{ $page.props.auth.user.name }}</Link>
                        <Link href="/logout" method="post" as="button" class="text-gray-500 text-sm">Salir</Link>
                    </template>
                    <template v-else>
                        <Link href="/login" class="text-gray-300 text-sm">Login</Link>
                        <Link href="/register" class="bg-white text-black px-3 py-1 text-sm">Registro</Link>
                    </template>

                    <button @click="showingMobileMenu = !showingMobileMenu" class="md:hidden p-2 text-gray-400">
                        <svg class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 6h16M4 12h16M4 18h16" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <div v-if="showingMobileMenu" class="md:hidden bg-gray-900 border-t border-gray-800">
            <div class="px-4 py-2 space-y-1">
                <Link href="/" class="block py-2 text-gray-300">Inicio</Link>
                <Link href="/shop" class="block py-2 text-gray-300">Catálogo</Link>
                <Link href="/about" class="block py-2 text-gray-300">Quiénes Somos</Link>
                <Link href="/contact" class="block py-2 text-gray-300">Contacto</Link>
            </div>
        </div>
    </nav>
</template>