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
  padding: 2.5rem 1.5rem;
  max-width: 900px;
  margin: 2.5rem auto;
  background: linear-gradient(135deg, #e0e7ff 0%, #f0fdfa 100%);
  border-radius: 1.5rem;
  box-shadow: 0 8px 32px 0 rgba(56,189,248,0.10), 0 2px 8px 0 rgba(31,38,135,0.08);
  font-family: 'Inter', 'Segoe UI', Arial, sans-serif;
  position: relative;
  z-index: 1;
  overflow: hidden;
}

.projects::before {
  content: "";
  position: absolute;
  top: -60px; left: -60px;
  width: 220px; height: 220px;
  background: radial-gradient(circle, #38bdf8 40%, transparent 70%);
  opacity: 0.15;
  z-index: 0;
  animation: float 7s infinite alternate;
}
@keyframes float {
  0% { transform: translateY(0);}
  100% { transform: translateY(30px);}
}

h2 {
  font-size: 2.3rem;
  margin-bottom: 2rem;
  font-weight: 800;
  letter-spacing: 0.03em;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  border-bottom: none;
  padding-bottom: 0;
  text-shadow: 0 2px 12px rgba(56,189,248,0.13);
}

.project-list {
  list-style: none;
  padding-left: 0;
  margin: 0;
  display: grid;
  gap: 2rem;
}

.project-item {
  background: rgba(255,255,255,0.85);
  padding: 1.7rem 1.3rem;
  border-radius: 1.1rem;
  border: 1.5px solid #38bdf8;
  box-shadow: 0 8px 24px rgba(56,189,248,0.10), 0 2px 8px rgba(31,38,135,0.08);
  backdrop-filter: blur(10px) saturate(120%);
  transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
  position: relative;
  z-index: 1;
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
}

.project-item:hover {
  transform: translateY(-6px) scale(1.02);
  box-shadow: 0 16px 40px 0 rgba(31, 38, 135, 0.18);
  border-color: #2563eb;
}

.project-title {
  font-size: 1.25rem;
  color: #2563eb;
  font-weight: 700;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 0.2rem;
  display: flex;
  align-items: center;
  gap: 0.7rem;
}

.project-title::before {
  content: "🛠️";
  font-size: 1.2rem;
  margin-right: 0.3rem;
}

.project-desc {
  color: #374151;
  line-height: 1.7;
  font-size: 1.08rem;
  background: rgba(255,255,255,0.6);
  border-radius: 0.5rem;
  padding: 0.7rem 0.8rem;
  box-shadow: 0 2px 8px rgba(56,189,248,0.07);
  transition: box-shadow 0.2s;
}

.project-desc:hover {
  box-shadow: 0 8px 24px rgba(56,189,248,0.13);
}

/* Animation */
.fade-stagger-enter-active {
  transition: all 0.6s cubic-bezier(.4,0,.2,1);
}
.fade-stagger-leave-active {
  transition: all 0.3s cubic-bezier(.4,0,.2,1);
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

@media (max-width: 600px) {
  .projects {
    padding: 1.2rem 0.5rem;
    font-size: 1rem;
  }
  h2 {
    font-size: 1.5rem;
  }
  .project-item {
    padding: 1rem 0.5rem;
  }
  .project-title {
    font-size: 1rem;
  }
  .project-desc {
    padding: 0.5rem 0.3rem;
    font-size: 0.98rem;
  }
}
</style>

