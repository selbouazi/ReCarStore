<script setup>
import Navbar from '@/Components/Layout/Navbar.vue';
import Footer from '@/Components/Layout/Footer.vue';

defineProps({
    cartCount: {
        type: Number,
        default: 0
    }
});
</script>

<template>
    <div class="min-h-screen flex flex-col bg-black text-white">
        <Navbar :cart-count="cartCount" />
        
        <main class="flex-grow">
            <slot />
        </main>
        
        <Footer />
    </div>
</template>