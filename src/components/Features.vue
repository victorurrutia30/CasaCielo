<!-- src/components/Features.vue -->
<template>
  <section class="py-12 bg-gray-100">
    <h2 class="text-2xl font-semibold text-center mb-8">Características</h2>
    <div class="max-w-4xl mx-auto grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <div v-for="f in features" :key="f.title" class="p-6 bg-white rounded-lg text-center shadow hover:shadow-lg transform hover:scale-105 transition duration-300 ease-in-out">
        <img :src="f.icon" class="w-16 h-16 mx-auto mb-4" />
        <h3 class="font-medium">{{ f.title }}</h3>
        <p class="text-sm text-gray-600">{{ f.desc }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      features: [
        { icon: '/icons/bed.svg', title: 'Habitaciones', desc: '3 habitaciones cómodas' },
        { icon: '/icons/view.svg', title: 'Vista al mar', desc: 'Panorámica y relajante' },
        { icon: '/icons/pool.svg', title: 'Piscina', desc: 'Privada con jacuzzi' },
        // …
      ]
    }
  }
}
</script>
