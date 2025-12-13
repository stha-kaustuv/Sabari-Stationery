<script setup>
import Sabari from "../assets/img/Sabari1.png";
</script>

<template>
  <header class="w-full bg-white shadow-md">
    <div class="max-w-7xl mx-auto flex items-center justify-between py-2 px-4">
      <div class="">
        <img :src="Sabari" alt="Sabari Logo" class="h-24" />
      </div>

      <nav class="flex items-center gap-12">
        <NuxtLink to="/" class="text-gray-700 hover:text-black font-medium"
          >Home</NuxtLink
        >
        <NuxtLink to="/about" class="text-gray-700 hover:text-black font-medium"
          >About</NuxtLink
        >

        <NuxtLink
          to="/products"
          class="text-gray-700 hover:text-black font-medium"
          >Products</NuxtLink
        >
        <NuxtLink
          to="/gallery"
          class="text-gray-700 hover:text-black font-medium"
          >Gallery</NuxtLink
        >
        <NuxtLink
          to="/contact"
          class="text-gray-700 hover:text-black font-medium"
          >Contact</NuxtLink
        >
        <button
          class="bg-black text-white px-4 py-2 rounded hover:bg-gray-800 transition"
        >
          Get Quote
        </button>
      </nav>
    </div>
  </header>
</template>

<style scoped>
/* Optional: add sticky header */
header {
  position: sticky;
  top: 0;
  z-index: 50;
}
</style>
