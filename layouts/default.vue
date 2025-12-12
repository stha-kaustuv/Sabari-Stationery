<script setup>
import { onMounted } from "vue";
import AppFooterVue from "../components/AppFooter.vue";
import AppHeaderVue from "../components/AppHeader.vue";
onMounted(() => {
  console.log("This is default.vue");
});
</script>

<template>
  <div>
    <AppHeaderVue />
    <slot />
    <AppFooterVue />
    <!-- <Toaster/> -->
  </div>
</template>
