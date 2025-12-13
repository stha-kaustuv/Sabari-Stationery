<script setup>
import blackSabari from "../assets/img/blackSabari.png";
</script>
<template>
  <div class="w-full bg-black p-2">
    <div class="max-w-7xl mx-auto py-2">
      <div class="text-gray-300 flex justify-between items-center">
        <div>
          <img :src="blackSabari" class="h-14" />
        </div>
        <div class="flex gap-5">
          <p>Facebook</p>
          <p>Instagram</p>
          <p>Whatsapp</p>
          <p>Whatsapp</p>
          <p>Whatsapp</p>
        </div>
      </div>
      <div
        class="flex mt-2 gap-[700px] text-gray-300 items-center cursor-pointer"
      >
        <div>
          <p>Kumarigal, chabahil</p>
          <p>Uma Maheswor Margha</p>
        </div>
        <div class="flex-1">
          <div class="flex justify-between">
            <NuxtLink class="hover:underline hover:text-white" to="/about"
              >Privacy Policy</NuxtLink
            >
            <NuxtLink class="hover:underline hover:text-white" to="/about"
              >About Us</NuxtLink
            >
            <NuxtLink class="hover:underline hover:text-white" to="/about"
              >Terms And Conditions</NuxtLink
            >
          </div>
          <div class="flex mt-3 justify-between">
            <NuxtLink class="hover:underline hover:text-white" to="/"
              >Terms And Conditions</NuxtLink
            >
            <NuxtLink class="hover:underline hover:text-white" to="/"
              >FAQ</NuxtLink
            >
            <NuxtLink class="hover:underline hover:text-white" to="/"
              >Contact Us</NuxtLink
            >
          </div>
        </div>
      </div>
    </div>
    <div class="w-full mt-5">
      <p
        class="w-80 mx-auto text-gray-200 text-sm cursor-pointer hover:text-white"
      >
        @2025 Sabari Stationery.All rights reserved
      </p>
    </div>
  </div>
</template>
