<script setup>
import Header from './components/Header.vue'
import About from './components/About.vue'
import Experience from './components/Experience.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
import Education from './components/Education.vue'
</script>

<template>
    <Header />
  

  <main>
    <About />
    <Experience />
    <Education />
    
    <Projects />
    <Skills />
    <Contact />
  </main>
</template>

<style scoped>
body {
  font-family: 'Segoe UI', sans-serif;
  margin: 0;
  background-color: #ffffff;
  color: #333;
}
main {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
}
</style>
