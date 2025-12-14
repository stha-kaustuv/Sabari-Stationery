<script setup>
import sketch from "../assets/img/notebooks/sketch2.jpg";
import copy from "../assets/img/notebooks/Copies.jpg";

</script>
<template>
  <div class="min-h-[100vh] max-w-[1280px] w-[1280px] shadow-md mx-auto px-8">
    <!-- Top Section -->
    <div class="flex gap-[100px] mt-4 items-center">
      <div class="max-w-[650px]">
        <p class="text-4xl font-bold text-black">Notebook</p>
        <p class="text-4xl font-bold text-black mt-1">Copy Factory</p>
        <p class="mt-3 text-gray-700">
          Sabari Stationery is a trusted notebook copy manufacturing factory
          dedicated to supplying high-quality copies for schools, offices and
          educational institutions. We focus on durability, neat finishing, and
          reliable bulk production.
        </p>
        <div class="mt-4">
          <NuxtLink to="/quote">
            <button class="bg-blue-800 text-white py-1 px-4 rounded-sm">
              Get a Quote
            </button>
          </NuxtLink>
        </div>
      </div>
      <div>
        <img :src="copy" class="h-[350px]" />
      </div>
    </div>

    <!-- About Section -->
    <div class="pt-6 flex gap-[100px] items-center">
      <div class="max-w-[650px]">
        <p class="text-3xl font-bold">About</p>
        <p class="mt-3 text-gray-700">
          Sabari Stationery is a notebook copy factory specializing in the
          production of school copies. With high-quality materials and efficient
          production processes, we ensure that every notebook meets the
          expectations of students, teachers, and institutions.
        </p>
        <p class="mt-2 text-gray-700">
          Our copies are designed for daily classroom and official use, offering strong
          binding, smooth paper, and clean layouts that support better learning
          experiences.
        </p>
      </div>
      <!-- abnout image section -->
      <div>
        <img :src="sketch" class="h-[350px]" />
      </div>
    </div>
  </div>
</template>
