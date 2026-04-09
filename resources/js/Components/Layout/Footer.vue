<script setup>
import { Link } from '@inertiajs/vue3';
</script>

<template>
    <footer class="bg-gray-900 border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4">
            <div class="grid md:grid-cols-3 gap-8 text-sm text-gray-400">
                <div>
                    <img src="/img/recarsore_logo.png" alt="ReCarStore" class="h-8 mb-4">
                    <p>Tu tienda de coches de segunda mano de confianza.</p>
                </div>
                <div>
                    <h3 class="text-white mb-2">Enlaces</h3>
                    <ul class="space-y-1">
                        <li><Link href="/shop">Catálogo</Link></li>
                        <li><Link href="/about">Quiénes Somos</Link></li>
                        <li><Link href="/contact">Contacto</Link></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-white mb-2">Legal</h3>
                    <ul class="space-y-1">
                        <li><Link href="/legal">Aviso Legal</Link></li>
                        <li><Link href="/privacy">Política de Privacidad</Link></li>
                        <li><Link href="/terms">Términos</Link></li>
                    </ul>
                </div>
            </div>
            <div class="mt-8 pt-4 border-t border-gray-800 text-center text-gray-500 text-sm">
                © 2026 ReCarStore
            </div>
        </div>
    </footer>
</template>