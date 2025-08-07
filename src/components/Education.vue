<template>
  <section class="education">
    <h2>Education & Certifications</h2>

    <transition-group name="fade-stagger" tag="ul" class="edu-list">
      <!-- Education -->
      <li class="edu-item" key="bsc">
        <div class="edu-title">
          <strong>B.Sc. in Computer Science and Engineering</strong>
          <span class="edu-period">2011 – 2016</span>
        </div>
        <p>Kwame Nkrumah University of Science and Technology (KNUST)</p>
      </li>

      <!-- Certifications -->
      <li v-for="(cert, index) in certifications" :key="index" class="edu-item">
        <div class="edu-title">
          <strong>{{ cert.name }}</strong>
          <span class="edu-period">{{ cert.validity }}</span>
        </div>
        <p v-if="cert.projectTitle"><strong>{{ cert.projectTitle }}</strong></p>
        <p v-if="cert.projectDesc">{{ cert.projectDesc }}</p>
      </li>
    </transition-group>
  </section>
</template>
<script setup>
const certifications = [
  {
    name: "AWS Certified Solutions Architect – Associate",
    validity: "Valid: March 2021 – March 2024",
    projectTitle: "SRE – FinTech Startup",
    projectDesc: "Implemented monitoring using Wazuh and CloudWatch. Reduced incidents by 30% and improved deployment reliability."
  },
  {
    name: "AWS Certified Cloud Practitioner",
    validity: "Valid: March 2021 – March 2024",
    projectTitle: "SRE – FinTech Startup",
    projectDesc: "Implemented monitoring using Wazuh and CloudWatch. Reduced incidents by 30% and improved deployment reliability."
  },
  {
    name: "Docker Certified Associate",
    validity: "No Expiry",
    projectTitle: "SRE – FinTech Startup",
    projectDesc: "Implemented monitoring using Wazuh and CloudWatch. Reduced incidents by 30% and improved deployment reliability."
  },
  {
    name: "Certified Kubernetes Application Developer (CKAD)",
    validity: "No Expiry",
    projectTitle: "SRE – FinTech Startup",
    projectDesc: "Implemented monitoring using Wazuh and CloudWatch. Reduced incidents by 30% and improved deployment reliability."
  },
  {
    name: "DevOps Engineer – MojoPay",
    validity: "Project Role",
    projectTitle: "Infrastructure & Security",
    projectDesc: "Led AWS infrastructure design and PCI compliance for a fintech startup. Automated CI/CD pipelines and managed cloud security."
  }
];
</script>
<style scoped>
.education {
  padding: 2rem;
  background-color: #f9f9f9;
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

.edu-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.edu-item {
  background: #fff;
  padding: 1.2rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
  border-radius: 6px;
  transition: all 0.3s ease;
}

.edu-title {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  flex-wrap: wrap;
  font-weight: 600;
  font-size: 1rem;
  color: #1f2937;
}

.edu-period {
  font-size: 0.9rem;
  color: #888;
}

.edu-item p {
  margin: 0.6rem 0 0;
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

