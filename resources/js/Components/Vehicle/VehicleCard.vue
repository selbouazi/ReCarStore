<script setup>
defineProps({
    vehicle: {
        type: Object,
        required: true
    }
});

const defaultImage = 'https://as1.ftcdn.net/jpg/10/22/24/80/220_F_1022248039_7LDxHRi3Mlt9BK3wzLBUGZp9XAO1gt2s.jpg';
</script>

<template>
    <div class="bg-gray-900 p-4">
        <img :src="vehicle.image || defaultImage" :alt="vehicle.marca + ' ' + vehicle.model" class="w-full rounded mb-4">
        <p class="text-gray-400 text-sm">{{ vehicle.marca }} {{ vehicle.model }}</p>
        <p class="text-lg font-bold">{{ vehicle.any }}</p>
        <p class="text-gray-500 text-sm">{{ vehicle.km?.toLocaleString() }} km</p>
        <div class="flex justify-between items-center mt-4">
            <span class="text-xl font-bold">{{ vehicle.preu }}€</span>
            <slot name="action">
                <button class="bg-white text-black px-4 py-1 text-sm">View</button>
            </slot>
        </div>
    </div>
</template>