<script setup lang="ts">
import NavBar from './components/NavBar.vue'
import Hero from './components/Hero.vue'
import Skills from './components/Skills.vue'
import About from './components/About.vue'
import Timeline from './components/Timeline.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="wrap">
    <NavBar />
    <hr class="section-divider" />
    <Hero />
    <hr class="section-divider" />
    <About />
    <hr class="section-divider" />
    <Skills />
    <hr class="section-divider" />
    <Timeline />
    <hr class="section-divider" />
    <Contact />
    <Footer />
  </div>
</template>
