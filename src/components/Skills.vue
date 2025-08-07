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
    skills: ["JavaScript", "PHP", "Python", "Bash", "Go"]
  },
  {
    name: "Frameworks & Tools",
    skills: ["Laravel", "Vue.js", "Node.js", "Apache Cordova", "Spring Boot"]
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

.skill-category {
  margin-bottom: 1.8rem;
}

.skill-category h3 {
  font-size: 1.2rem;
  color: #1f2937;
  margin-bottom: 0.5rem;
}

.skill-tags {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  padding: 0;
  margin: 0;
}

.skill-tags li {
  background-color: #1a73e8;
  color: white;
  padding: 0.4rem 0.8rem;
  border-radius: 20px;
  font-size: 0.9rem;
  transition: background-color 0.3s ease;
}

.skill-tags li:hover {
  background-color: #155ab6;
}
</style>
