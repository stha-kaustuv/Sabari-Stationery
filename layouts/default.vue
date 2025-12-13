<script setup>
import { onMounted } from "vue";
import AppFooterVue from "../components/AppFooter.vue";
import AppHeaderVue from "../components/AppHeader.vue";
onMounted(() => {
  console.log("This is default.vue");
});
</script>

<template>
  <div class="p-14 h-full bg-gray-300">
    <div class="shadow-md bg-white h-screen relative">
      <AppHeaderVue />
      <slot />
      <div class="w-full border absolute bottom-0 z-40">
        <AppFooterVue />
      </div>

      <!-- SVG positioned relative to this box -->
      <div
        class="absolute -bottom-14 -right-14 w-30 h-30 text-white pointer-events-none"
      >
        <svg viewBox="0 0 100 100" fill="currentColor">
          <path
            d="M50 5 C54 25, 75 25, 78 35
             C82 45, 95 50, 70 58
             C60 62, 62 85, 50 75
             C38 85, 40 62, 30 58
             C5 50, 18 45, 22 35
             C25 25, 46 25, 50 5 Z"
          />
        </svg>
      </div>
      <!-- <div
        class="star absolute -bottom-12 -right-12 w-30 h-30 text-white pointer-events-none"
      ></div> -->
    </div>
  </div>
</template>
<style>
.star {
  width: 110px;
  height: 110px;
  /* z-index: 40px; */
  background-color: #ffff; /* yellow-400 */
  clip-path: polygon(
    50% 0%,
    61% 30%,
    98% 30%,
    68% 50%,
    79% 90%,
    50% 70%,
    21% 90%,
    32% 57%,
    2% 30%,
    39% 30%
  );
}
</style>
