<script setup>
import { Link } from '@inertiajs/vue3';
</script>

<template>
    <div class="min-h-screen flex flex-col bg-black text-white">
        <nav class="bg-gray-900 border-b border-gray-800">
            <div class="max-w-7xl mx-auto px-4">
                <div class="flex justify-between h-14">
                    <div class="flex items-center">
                        <Link href="/" class="flex items-center">
                            <img src="/img/recarsore_logo.png" alt="ReCarStore" class="h-10 w-auto">
                        </Link>
                    </div>
                    <div class="flex items-center">
                        <Link href="/" class="text-gray-400 text-sm">Tornar</Link>
                    </div>
                </div>
            </div>
        </nav>

        <div class="flex-grow flex items-center justify-center px-4 py-12">
            <div class="w-full max-w-md">
                <div class="bg-gray-900 p-8">
                    <slot />
                </div>
            </div>
        </div>
    </div>
</template>