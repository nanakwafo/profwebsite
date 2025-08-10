<script setup>
import Header from './components/Header.vue'
import About from './components/About.vue'
import Experience from './components/Experience.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
import Education from './components/Education.vue'

import Achievement from './components/Achievement.vue'
</script>

<template>
  <div class="layout">
    <Header />
    <main class="main-content">
      <section id="about"><About /></section>
      <section id="achievement"><Achievement /></section>
      <section id="experience"><Experience /></section>
      <section id="education"><Education /></section>
      <section id="projects"><Projects /></section>
      <section id="skills"><Skills /></section>
      <section id="contact"><Contact /></section>
    </main>
  </div>
</template>

<style scoped>

.layout {
  font-family: 'Segoe UI', sans-serif;
  background-color: #f9f9f9;
  color: #222;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.main-content {
  /* max-width: 1000px; */
  /* width: 100%; */
  margin: 0 auto;
  padding: 2rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 3rem;
}

section {
  background-color: #ffffff;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
  scroll-margin-top: 80px;
}

@media (min-width: 768px) {
  .main-content {
    padding: 3rem 2rem;
  }
  section {
    padding: 3rem;
  }
}
</style>
