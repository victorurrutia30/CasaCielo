<!-- src/App.vue -->
<template>
  <HeroSection/>
  <Gallery/>
  <Features/>
  <FormEmbed/>
  <CalendarEmbed/>
  <FooterSection/>
</template>

<script>
import HeroSection from './components/HeroSection.vue'
import Gallery from './components/Gallery.vue'
import Features from './components/Features.vue'
import FormEmbed from './components/FormEmbed.vue'
import CalendarEmbed from './components/CalendarEmbed.vue'
import FooterSection from './components/FooterSection.vue'

export default {
  components: {
    HeroSection, Gallery, Features, FormEmbed, CalendarEmbed, FooterSection
  }
}
</script>
