<!-- src/components/Gallery.vue -->
<template>
  <div class="max-w-5xl mx-auto py-12">
    <h2 class="text-2xl font-semibold mb-6 text-center">Galería</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
      <div v-for="(img, i) in images" :key="i" @click="open(i)" class="cursor-pointer">
        <img :src="img" class="w-full h-48 object-cover rounded-lg shadow" />
      </div>
    </div>

    <!-- Modal simple -->
    <div v-if="current !== null" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center">
      <img :src="images[current]" class="max-h-full max-w-full rounded" />
      <button @click="current = null" class="absolute top-4 right-4 text-white text-2xl">&times;</button>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup() {
    const images = [
      '/gallery/1.jpg',
      '/gallery/2.jpg',
      '/gallery/3.jpg',
      // …añade más
    ]
    const current = ref(null)
    const open = i => current.value = i
    return { images, current, open }
  }
}
</script>
