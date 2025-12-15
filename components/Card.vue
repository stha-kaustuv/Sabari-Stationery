<script setup>
const props = defineProps({
  showButton: {
    type: Boolean,
    default: true,
  },
  showImage: {
    type: Boolean,
    default: true,
  },
  showSchool: {
    type: Boolean,
    default: false,
  },
  school: {
    type: String,
  },
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
    <div class="p-3 rounded-sm border border-gray-200 min-h-[100px] min-w-62.5">
      <img
        v-if="showImage"
        :src="props.image"
        class="h-[200px] object-contain"
      />
      <div class="w-full flex justify-center">
        <button
          v-if="showButton"
          class="border bg-blue-900 py-1 px-2 rounded-sm mt-3 cursor-pointer text-white"
        >
          Learn More
        </button>
      </div>
      <div class="h-full flex flex-col justify-between">
        <p class="text-2xl text-center">{{ props.school }}</p>
      </div>
    </div>
  </div>
</template>
