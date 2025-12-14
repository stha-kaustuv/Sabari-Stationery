<script setup>
import { ref } from "vue";
import { Swiper } from "swiper/vue";
import { SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/effect-coverflow";
import { EffectCoverflow, Navigation } from "swiper/modules";

// --- CHANGE MADE HERE ---
// Import Swiper modules from 'swiper/modules' instead of the top-level 'swiper'
// import { Navigation, EffectCoverflow } from "swiper/modules";
// --- END CHANGE ---

const props = defineProps({
  products: { type: Array, required: true },
});

const activeIndex = ref(0);

const handleSlideChange = (swiper) => {
  activeIndex.value = swiper.realIndex;
};
</script>

<template>
  <client-only>
    <Swiper
      class="animated-slider"
      :modules="[Navigation, EffectCoverflow]"
      :effect="'coverflow'"
      :navigation="true"
      :loop="true"
      @slide-change="handleSlideChange"
      :centered-slides="true"
      :grab-cursor="true"
      :coverflow-effect="{
        rotate: 0,
        stretch: -20,
        depth: 80,
        modifier: 2,
        slideShadows: false,
      }"
      :breakpoints="{
        640: { slidesPerView: 1, spaceBetween: 10 },
        768: { slidesPerView: 2, spaceBetween: 20 },
        1024: { slidesPerView: 3, spaceBetween: 30 },
        1200: { slidesPerView: 4, spaceBetween: 30 },
      }"
    >
      <SwiperSlide v-for="(slide, index) in products" :key="slide.id">
        <div class="flex justify-center">
          <nuxt-link :to="`/book/${slide.id}`">
            <img
              :src="slide.image"
              alt="Image"
              class="w-[298px] h-[438px] object-cover rounded-lg shadow-lg"
            />
          </nuxt-link>
        </div>

        <div class="pt-4 flex justify-center" v-if="index === activeIndex">
          <nuxt-link :to="`/book/${slide.id}`">
            <h1
              class="w-[300px] h-[38px] overflow-hidden text-center text-[24px]"
            >
              {{ slide.name }}
            </h1>
          </nuxt-link>
        </div>
      </SwiperSlide>
    </Swiper>
  </client-only>
</template>
<style>
.animated-slider {
  position: relative;
}

/* --- PREVIOUS BUTTON STYLES (Consolidated and Adjusted) --- */

/* Styles for the NEXT button */
.animated-slider .swiper-button-next {
  /* Positioning */
  position: absolute;
  top: 50%;
  right: calc(50% - 160px); /* Adjusted to 70px to bring it closer */
  transform: translateY(-50%);

  /* Appearance */
  height: 30px;
  width: 30px;
  border-radius: 100%;
  background: black; /* Set background to white */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2); /* Add subtle shadow for visibility */
  --swiper-navigation-size: 16px; /* Arrow size */
  color: white; /* Arrow color set to black */
}

/* Styles for the PREV button */
.animated-slider .swiper-button-prev {
  /* Positioning */
  position: absolute;
  top: 50%;
  left: calc(50% - 160px); /* Adjusted to 70px to bring it closer */
  transform: translateY(-50%);

  /* Appearance */
  height: 30px;
  width: 30px;
  border-radius: 100%;
  background: black;

  --swiper-navigation-size: 16px;
  color: white;
}

.animated-slider .swiper-button-prev:after,
.animated-slider .swiper-button-next:after {
  color: black;
}

@media (max-width: 640px) {
  .animated-slider .swiper-button-next,
  .animated-slider .swiper-button-prev {
    height: 28px;
    width: 28px;
    right: 10px;
    left: 10px;
  }
}
</style>
