<template>
  <h1>This is app header</h1>
</template>
<script setup>
import { onMounted } from "vue";

onMounted(() => {
  console.log("This is app header");
});
</script>
