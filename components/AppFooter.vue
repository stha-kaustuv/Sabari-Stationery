<script setup>
import blackSabari from "../assets/img/blackSabari.png";
import blackSabari2 from "../assets/img/blackSabari2.png";
import facebook from "../assets/img/facebook.png";
import viber from "../assets/img/viber.png";
import whatsapp from "../assets/img/whatsapp.png";
import instagram from "../assets/img/instagram.jpeg";
</script>
<template>
  <div class="w-full bg-black p-4">
    <div class="max-w-7xl mx-auto py-2 shadow-md">
      <div class="text-gray-300 flex justify-between items-center">
        <div class="">
          <img :src="blackSabari2" class="h-24" />
        </div>
        <div class="flex gap-5">
          <a
            href="https://www.facebook.com/addwet.shrestha/"
            target="_blank"
            rel="noopener noreferrer"
            ><img :src="facebook" class="h-8"
          /></a>
          <a
            href="https://wa.me/9779841647263"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img :src="whatsapp" class="h-8" />
          </a>
          <a
            href="https://www.instagram.com/addwetkrishna/"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img :src="instagram" class="h-8" />
          </a>

          <a
            href="viber://chat?number=9779841647263"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img :src="viber" class="h-8" />
          </a>
        </div>
      </div>
      <div
        class="flex mt-2 gap-[670px] text-gray-300 items-center cursor-pointer"
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
