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
        <p>University of Mines and Technology (UMAT)</p>
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
    validity: "Valid: March 2021 – March 2024", },
  {
    name: "AWS Certified Cloud Practitioner",
    validity: "Valid: March 2021 – March 2024",
    },
  {
    name: "Docker Certified Associate",
    validity: "No Expiry",
    },
  {
    name: "Certified Kubernetes Application Developer (CKAD)",
    validity: "No Expiry",
  }
];
</script>
<style scoped>
.education {
  padding: 2.5rem 1.5rem;
  background: linear-gradient(135deg, #e0e7ff 0%, #f0fdfa 100%);
  max-width: 900px;
  margin: 2.5rem auto;
  border-radius: 1.5rem;
  box-shadow: 0 8px 32px 0 rgba(56,189,248,0.10), 0 2px 8px 0 rgba(31,38,135,0.08);
  font-family: 'Inter', 'Segoe UI', Arial, sans-serif;
  position: relative;
  z-index: 1;
  overflow: hidden;
}

.education::before {
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
  font-size: 2.4rem;
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

.edu-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
  display: grid;
  gap: 2rem;
}

.edu-item {
  background: rgba(255,255,255,0.85);
  padding: 1.7rem 1.3rem;
  margin: 0;
  box-shadow: 0 8px 24px rgba(56,189,248,0.10), 0 2px 8px rgba(31,38,135,0.08);
  border-radius: 1.1rem;
  border: 1.5px solid #38bdf8;
  backdrop-filter: blur(10px) saturate(120%);
  transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
  position: relative;
  z-index: 1;
}

.edu-item:hover {
  transform: translateY(-6px) scale(1.02);
  box-shadow: 0 16px 40px 0 rgba(31, 38, 135, 0.18);
  border-color: #2563eb;
}

.edu-title {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  flex-wrap: wrap;
  font-weight: 700;
  font-size: 1.08rem;
  color: #2563eb;
  margin-bottom: 0.5rem;
}

.edu-title strong {
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 800;
  font-size: 1.15rem;
}

.edu-period {
  font-size: 0.98rem;
  color: #38bdf8;
  font-weight: 600;
  background: rgba(56,189,248,0.08);
  border-radius: 0.5rem;
  padding: 0.2rem 0.7rem;
}

.edu-item p {
  margin: 0.7rem 0 0;
  color: #374151;
  line-height: 1.7;
  font-size: 1.05rem;
  background: rgba(255,255,255,0.6);
  border-radius: 0.5rem;
  padding: 0.7rem 0.8rem;
  box-shadow: 0 2px 8px rgba(56,189,248,0.07);
  transition: box-shadow 0.2s;
}

.edu-item p strong {
  color: #2563eb;
  font-weight: 700;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.edu-item p:hover {
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
  .education {
    padding: 1.2rem 0.5rem;
    font-size: 1rem;
  }
  h2 {
    font-size: 1.6rem;
  }
  .edu-item {
    padding: 1rem 0.5rem;
  }
  .edu-title strong {
    font-size: 1rem;
  }
  .edu-period {
    font-size: 0.9rem;
    padding: 0.15rem 0.5rem;
  }
  .edu-item p {
    padding: 0.5rem 0.3rem;
    font-size: 0.98rem;
  }
}


</style>

