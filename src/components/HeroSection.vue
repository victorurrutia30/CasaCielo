<!-- src/components/HeroSection.vue -->
<template>
  <section class="h-screen bg-cover bg-center flex items-center justify-center" style="background-image:url('/hero.jpeg')">
    <div class="text-center bg-white bg-opacity-70 p-8 rounded-lg">
      <h1 class="text-4xl md:text-6xl font-bold mb-4 typing">Rancho Playa Elegante</h1>
      <p class="text-lg text-gray-700 dark:text-gray-300 mt-2">Tu refugio de lujo frente al mar</p>
      <button class="px-6 py-3 bg-teal-500 text-white rounded hover:bg-teal-600 transition">
        Contáctanos
      </button>
    </div>
  </section>
</template>

<style scoped>
@keyframes typing {
  from { width: 0 }
  to   { width: 100% }
}
@keyframes blink {
  50% { border-color: transparent }
}
.typing {
  overflow: hidden;
  white-space: nowrap;
  border-right: 2px solid currentColor;
  animation: typing 3s steps(30,end), blink .75s step-end infinite;
}
</style>
