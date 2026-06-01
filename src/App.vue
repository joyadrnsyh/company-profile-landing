<script setup lang="ts">
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Team from './components/Team.vue'
import Testimonials from './components/Testimonials.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>
    <Hero />
    <About />
    <Services />
    <Team />
    <Testimonials />
    <Contact />
  </main>
  <footer>
    <Footer />
  </footer>
</template>

<style scoped>
main {
  width: 100%;
  overflow: hidden;
}
</style>
