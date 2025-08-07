<template>
  <section class="projects">
    <h2>Personal Projects</h2>
    <transition-group name="fade-stagger" tag="ul" class="project-list">
      <li v-for="(project, index) in personalProjects" :key="index" class="project-item">
        <strong class="project-title">{{ project.title }}</strong>
        <p class="project-desc">{{ project.description }}</p>
      </li>
    </transition-group>
  </section>
</template>
<script setup>
const personalProjects = [
  {
    title: "WhatsApp Shop AI Assistant",
    description:
      "A chatbot assistant that helps small businesses in Ghana sell products via WhatsApp. Built with Laravel + GPT."
  },
  {
    title: "Urbanhire Equipment Rentals",
    description:
      "An inventory and rental system for scaffolds, wheelbarrows, and construction tools."
  }
];
</script>

<style scoped>
.projects {
  padding: 2rem;
  max-width: 800px;
  margin: 0 auto;
}

h2 {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  color: #333;
  border-bottom: 2px solid #ddd;
  padding-bottom: 0.5rem;
}

.project-list {
  list-style: none;
  padding-left: 0;
  margin: 0;
}

.project-item {
  background: #f9f9f9;
  padding: 1rem 1.2rem;
  margin-bottom: 1.2rem;
  border-left: 4px solid #1a73e8;
  border-radius: 6px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  transition: all 0.3s ease;
}

.project-title {
  font-size: 1.1rem;
  color: #1f2937;
}

.project-desc {
  margin-top: 0.4rem;
  color: #555;
  line-height: 1.6;
}

/* Animation */
.fade-stagger-enter-active {
  transition: all 0.6s ease;
}
.fade-stagger-leave-active {
  transition: all 0.3s ease;
  opacity: 0;
  transform: translateY(20px);
}
.fade-stagger-enter-from {
  opacity: 0;
  transform: translateY(20px);
}
.fade-stagger-enter-to {
  opacity: 1;
  transform: translateY(0);
}
</style>

