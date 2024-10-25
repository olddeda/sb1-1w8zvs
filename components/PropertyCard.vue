<template>
  <div class="bg-white rounded-lg shadow-lg overflow-hidden">
    <div class="relative">
      <img :src="property.image" :alt="property.title" class="w-full h-64 object-cover">
      <div class="absolute top-4 right-4 bg-white px-3 py-1 rounded-full text-sm font-medium">
        Эконом-класс
      </div>
    </div>
    <div class="p-6">
      <h3 class="text-xl font-semibold mb-2">{{ property.title }}</h3>
      <p class="text-gray-600 mb-4">{{ property.description }}</p>
      <div class="flex flex-wrap gap-2 mb-4">
        <span v-for="(feature, index) in property.features" :key="index"
          class="bg-gray-100 px-3 py-1 rounded-full text-sm">
          {{ feature }}
        </span>
      </div>
      <div class="flex gap-2">
        <button class="bg-blue-600 text-white px-4 py-2 rounded-lg flex items-center gap-2">
          <span>Позвонить</span>
        </button>
        <button class="bg-gray-100 px-4 py-2 rounded-lg flex items-center gap-2">
          <span>Написать</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  property: {
    type: Object,
    required: true
  }
})
</script>