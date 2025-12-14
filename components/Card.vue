<script setup>
const props = defineProps({
  id: {
    type: Number,
    required: true,
  },
  image: {
    type: String,
  },
});
</script>

<template>
  <div class="py-4">
    <div class="p-3 rounded-sm border border-gray-200">
      <img :src="props.image" class="h-[200px] object-contain" />
      <div class="w-full flex justify-center">
        <button
          class="border bg-blue-900 py-1 px-2 rounded-sm mt-3 cursor-pointer text-white"
        >
          Learn More
        </button>
      </div>
    </div>
  </div>
</template>
