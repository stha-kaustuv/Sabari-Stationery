<script setup>
import sketch from "../assets/img/notebooks/sketch2.jpg";
import copy2 from "../assets/img/notebooks/Copy2.jpg";
import notebook from "../assets/img/notebooks/Notebook.jpg";
import personalized from "../assets/img/notebooks/PersonalisedCopy.png";
import sketch2 from "../assets/img/notebooks/Sketch.jpg";
import copy from "../assets/img/notebooks/Copies.jpg";
import Card from "~/components/Card.vue";
import AnimatedSlider from "~/components/AnimatedSlider.vue";

const products = [
  {
    id: 1,
    image: personalized,
    name: "Personalized",
  },
  {
    id: 2,
    image: copy2,
    name: "Copy",
  },
  {
    id: 3,
    image: notebook,
    name: "Notebook",
  },
  {
    id: 4,
    image: copy,
    name: "Drawing Copy",
  },
  {
    id: 7,
    image: personalized,
    name: "Personalized",
  },
  {
    id: 5,
    image: sketch,
    name: "Sketch",
  },
  {
    id: 6,
    image: sketch2,
    name: "Notebook",
  },
];
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
          Our copies are designed for daily classroom and official use, offering
          strong binding, smooth paper, and clean layouts that support better
          learning experiences.
        </p>
      </div>
      <!-- abnout image section -->
      <div>
        <img :src="sketch" class="h-[350px]" />
      </div>
    </div>

    <div class="w-full bg-blue-900 p-[1px]"></div>

    <!-- Product Section -->
    <div class="py-6">
      <p class="text-3xl text-gray-700 font-bold">Products</p>
      <div class="flex gap-[70px]">
        <div
          v-for="(product, index) in products.slice(0, 4)"
          class="pt-6"
          :key="index"
        >
          <Card :id="product.id" :image="product.image" />
        </div>
      </div>
    </div>
    <div class="w-full bg-blue-900 p-[1px] my-2"></div>

    <div class="py-8 bg-custom-gradient">
      <div
        class="container mx-auto flex flex-col items-center space-y-4 text-center"
      >
        <h1
          class="text-center font-semibold italic font-roboto text-2xl md:text-[40px]"
        >
          Gallery
        </h1>
        <p class="text-gray-500 text-sm md:text-[18px] max-w-[786px]">
          At Sabari Stationery Udhyog, we showcase the quality and craftsmanship
          of our notebooks, copies, and stationery. Explore our gallery to see
          durable, beautifully finished products made for schools and
          institutions.
        </p>
      </div>
      <!-- Slider -->
      <div
        class="container mx-auto px-4 sm:px-8 md:px-12 lg:px-16 xl:px-20 py-4 relative pt-[34px]"
      >
        <AnimatedSlider :products="products" />
        <!--------------------------- two sides gradients ---------------------------->
        <!-- <div class="bg-ourPicksGradients-g1 opacity-75   w-[192px] h-[339px] z-40 absolute top-[93px]"></div>
        <div class="bg-ourPicksGradients-g1 opacity-75   w-[192px] h-[339px] z-40 absolute top-[93px] right-[80px]"></div> -->
      </div>
    </div>
  </div>
</template>

<style>
.bg-custom-gradient {
  background: linear-gradient(
    to right,
    rgba(255, 255, 255, 0.8),
    /* Slightly white at the left */ rgba(209, 231, 255, 255),
    /* More white at the middle */ rgba(255, 255, 255, 0.8)
      /* Slightly white at the right */
  );
}
</style>
