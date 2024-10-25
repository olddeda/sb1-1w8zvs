<template>
  <div class="min-h-screen bg-gray-50">
    <header class="bg-white shadow-sm">
      <div class="max-w-7xl mx-auto px-4 py-4">
        <h1 class="text-2xl font-bold text-center">ЛУЧШИЕ НОВОСТРОЙКИ ЭКОНОМ-КЛАССА</h1>
      </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 py-8">
      <div class="flex flex-wrap gap-4 mb-6">
        <button 
          v-for="location in ['Шоссе', 'Новорижское', 'Ярославское']" 
          :key="location"
          class="px-4 py-2 rounded-full bg-white shadow-sm hover:bg-gray-50"
        >
          {{ location }}
        </button>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <PropertyCard
          v-for="property in properties"
          :key="property.id"
          :property="property"
        />
      </div>
    </main>
  </div>
</template>

<script setup>
const properties = ref([
  {
    id: 1,
    title: 'Квартиры с отделкой в ЖК «Зеленый Город»',
    description: 'Жилой комплекс эконом класса в 40 км от МКАД по Ленинградскому или Дмитровскому шоссе.',
    image: 'https://placehold.co/600x400',
    features: ['Школа', 'Детский сад', '2 озера', 'Схема проезда']
  },
  {
    id: 2,
    title: 'Квартиры с отделкой в ЖК «Зеленый Город»',
    description: 'Жилой комплекс эконом класса в 40 км от МКАД по Ленинградскому или Дмитровскому шоссе.',
    image: 'https://placehold.co/600x400',
    features: ['Школа', 'Детский сад', '2 озера', 'Схема проезда']
  },
  {
    id: 3,
    title: 'Квартиры с отделкой в ЖК «Зеленый Город»',
    description: 'Жилой комплекс эконом класса в 40 км от МКАД по Ленинградскому или Дмитровскому шоссе.',
    image: 'https://placehold.co/600x400',
    features: ['Школа', 'Детский сад', '2 озера', 'Схема проезда']
  }
])
</script>