<!-- src/App.vue -->
<template>
<Navbar/>
  <HeroSection id="hero"/>
  <Gallery id="gallery"/>
  <Features id="features"/>
  <FormEmbed/>
  <CalendarEmbed/>
  <FooterSection/>
</template>

<script>

import Navbar from './components/Navbar.vue'
import HeroSection from './components/HeroSection.vue'
import Gallery from './components/Gallery.vue'
import Features from './components/Features.vue'
import FormEmbed from './components/FormEmbed.vue'
import CalendarEmbed from './components/CalendarEmbed.vue'
import FooterSection from './components/FooterSection.vue'

export default {
  components: {
    Navbar, HeroSection, Gallery, Features, FormEmbed, CalendarEmbed, FooterSection
  }
}
</script>
