<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import APropos from './components/APropos.vue'
import Competences from './components/Competences.vue'
import Slider from './components/Slider.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="overflow-x-hidden">
  <Navbar />
  <div id="home">
  <Hero />
  </div>
  <div id="apropos">
    <APropos />
  </div>
  <div id="competences">
    <Competences />
  </div>
  <div id="projets">
    <Slider />
  </div>
  <div id="contact">
    <Contact />
  </div>
  <Footer />
  </div>
</template>