<script setup>
import Sabari from "../assets/img/Sabari1.png";
</script>

<template>
  <header class="w-full bg-white shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto flex items-center justify-between py-2 px-4">
      <img :src="Sabari" alt="Sabari Logo" class="h-24" />

      <nav class="flex items-center gap-12">
        <NuxtLink
          to="/"
          exact-active-class="text-black border-b-2 border-black"
          class="text-gray-700 hover:text-black font-medium pb-1"
        >
          Home
        </NuxtLink>

        <NuxtLink
          to="/about"
          active-class="text-black border-b-2 border-black"
          class="text-gray-700 hover:text-black font-medium pb-1"
        >
          About
        </NuxtLink>

        <NuxtLink
          to="/products"
          active-class="text-black border-b-2 border-black"
          class="text-gray-700 hover:text-black font-medium pb-1"
        >
          Products
        </NuxtLink>

        <NuxtLink
          to="/gallery"
          active-class="text-black border-b-2 border-black"
          class="text-gray-700 hover:text-black font-medium pb-1"
        >
          Gallery
        </NuxtLink>

        <NuxtLink
          to="/contact"
          active-class="text-black border-b-2 border-black"
          class="text-gray-700 hover:text-black font-medium pb-1"
        >
          Contact
        </NuxtLink>

        <button
          class="bg-black text-white px-4 py-2 rounded hover:bg-gray-800 transition"
        >
          Get Quote
        </button>
      </nav>
    </div>
  </header>
</template>
