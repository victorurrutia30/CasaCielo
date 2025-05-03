<template>
  <nav class="fixed w-full bg-white dark:bg-gray-900 shadow z-50">
    <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
      <a href="#" class="text-xl font-bold text-teal-600 dark:text-teal-400">Rancho Playa</a>
      <div class="flex items-center space-x-4">
        <a href="#hero" class="hover:text-teal-500">Inicio</a>
        <a href="#features" class="hover:text-teal-500">Características</a>
        <a href="#gallery" class="hover:text-teal-500">Galería</a>
        <button @click="toggleDark"
                class="p-2 rounded focus:outline-none focus:ring-2 focus:ring-teal-500">
          <span v-if="isDark">🌞</span>
          <span v-else>🌙</span>
        </button>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted } from 'vue'
const isDark = ref(document.documentElement.classList.contains('dark'))
function toggleDark() {
  document.documentElement.classList.toggle('dark')
  isDark.value = !isDark.value
}
onMounted(() => {
  // Si quieres sincronizar con preferencia del sistema:
  if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
    document.documentElement.classList.add('dark')
    isDark.value = true
  }
})
</script>

<style scoped>
a { @apply text-gray-700 dark:text-gray-300 transition; }
</style>
