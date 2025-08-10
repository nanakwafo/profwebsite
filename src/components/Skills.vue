<template>
  <section class="skills">
    <h2>Skills</h2>
    <div class="skill-category" v-for="(category, index) in skillCategories" :key="index">
      <h3>{{ category.name }}</h3>
      <ul class="skill-tags">
        <li v-for="(skill, i) in category.skills" :key="i">{{ skill }}</li>
      </ul>
    </div>
  </section>
</template>

<script setup>
const skillCategories = [
  {
    name: "Cloud Platforms",
    skills: ["AWS", "Azure", "Google Cloud", "EC2", "S3", "CloudWatch", "WAF", "ECS", "EKS"]
  },
  {
    name: "DevOps & Automation",
    skills: ["Docker", "Kubernetes", "Terraform", "GitHub Actions", "GitLab CI", "Jenkins", "Ansible"]
  },
  {
    name: "Programming Languages",
    skills: ["JavaScript", "PHP", "Python", "Bash", "C#"]
  },
  {
    name: "Frameworks & Tools",
    skills: ["Laravel", "Vue.js", "Node.js", "Apache Cordova", "Spring Boot","wordpress"]
  },
  {
    name: "Certifications",
    skills: [
      "AWS Certified Solutions Architect",
      "AWS Cloud Practitioner",
      "Docker Certified Associate",
      "CKAD"
    ]
  }
];
</script>

<style scoped>
.skills {
  padding: 2.5rem 1.5rem;
  max-width: 850px;
  margin: 2.5rem auto;
  background: linear-gradient(135deg, #e0e7ff 0%, #f0fdfa 100%);
  border-radius: 1.5rem;
  box-shadow: 0 8px 32px 0 rgba(56,189,248,0.10), 0 2px 8px 0 rgba(31,38,135,0.08);
  font-family: 'Inter', 'Segoe UI', Arial, sans-serif;
  position: relative;
  z-index: 1;
  overflow: hidden;
}

.skills::before {
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

.skill-category {
  margin-bottom: 2.2rem;
  background: rgba(255,255,255,0.85);
  border-radius: 1.1rem;
  box-shadow: 0 4px 16px rgba(56,189,248,0.10);
  padding: 1.2rem 1rem;
  position: relative;
  z-index: 1;
  transition: box-shadow 0.2s, transform 0.2s;
}

.skill-category:hover {
  box-shadow: 0 12px 32px rgba(56,189,248,0.15);
  transform: translateY(-4px) scale(1.01);
}

.skill-category h3 {
  font-size: 1.18rem;
  color: #2563eb;
  font-weight: 700;
  margin-bottom: 0.7rem;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.skill-tags {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  gap: 0.7rem;
  padding: 0;
  margin: 0;
}

.skill-tags li {
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  color: #fff;
  padding: 0.5rem 1.1rem;
  border-radius: 2rem;
  font-size: 1rem;
  font-weight: 600;
  box-shadow: 0 2px 8px rgba(56,189,248,0.09);
  transition: background 0.3s, transform 0.2s;
  cursor: pointer;
  border: none;
  outline: none;
}

.skill-tags li:hover {
  background: linear-gradient(90deg, #2563eb 0%, #38bdf8 100%);
  transform: scale(1.08);
  box-shadow: 0 6px 18px rgba(56,189,248,0.13);
}

@media (max-width: 600px) {
  .skills {
    padding: 1.2rem 0.5rem;
    font-size: 1rem;
  }
  h2 {
    font-size: 1.5rem;
  }
  .skill-category {
    padding: 0.8rem 0.3rem;
  }
  .skill-category h3 {
    font-size: 1rem;
  }
  .skill-tags li {
    font-size: 0.95rem;
    padding: 0.4rem 0.7rem;
  }
}
</style>
