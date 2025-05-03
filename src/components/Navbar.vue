<template>
  <nav class="fixed top-0 left-0 w-full bg-white dark:bg-gray-900 shadow z-50">

    <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
      <!-- Logo -->
      <a href="#" class="text-2xl font-bold text-teal-600 dark:text-teal-400">Rancho Playa</a>

      <!-- Botón hamburguesa (solo en sm) -->
      <button
        @click="menuOpen = !menuOpen"
        class="sm:hidden p-2 focus:outline-none focus:ring-2 focus:ring-teal-500"
      >
        <i :class="menuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
      </button>

      <!-- Links + toggle dark (oculto en móvil hasta abrir) -->
      <div
        class="flex flex-col sm:flex-row sm:items-center sm:space-x-6 space-y-2 sm:space-y-0"
      >
        <a href="#hero"      class="block text-gray-700 dark:text-gray-300 hover:text-teal-500 transition">Inicio</a>
        <a href="#features"  class="block text-gray-700 dark:text-gray-300 hover:text-teal-500 transition">Características</a>
        <a href="#gallery"   class="block text-gray-700 dark:text-gray-300 hover:text-teal-500 transition">Galería</a>
        <button
          @click="toggleDark"
          class="block p-2 rounded focus:outline-none focus:ring-2 focus:ring-teal-500"
        >
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
const menuOpen = ref(false)

function toggleDark() {
  document.documentElement.classList.toggle('dark')
  isDark.value = !isDark.value
}

onMounted(() => {
  if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
    document.documentElement.classList.add('dark')
    isDark.value = true
  }
})
</script>

<style scoped>
/* Retén tu estilo de enlaces */
a { @apply transition; }
/* FontAwesome ya está cargado via index.html */
</style>
