<template>
  <section class="experience">
    <h2>
      <span class="icon-briefcase"></span>
      Experience
    </h2>
    <transition-group name="fade-stagger" tag="ul" class="job-list">
      <li v-for="(job, index) in jobs" :key="index" class="job-item">
        <div class="job-card">
          <div class="job-header">
            <span class="icon-company"></span>
            <div>
              <strong class="job-title">{{ job.title }}</strong>
              <div class="job-company">{{ job.company }} <span class="job-location">• {{ job.location }}</span></div>
              <div class="job-dates">{{ job.dates }}</div>
            </div>
          </div>
          <ul class="job-details">
            <li v-for="(detail, i) in job.details" :key="i">
              <span class="icon-dot"></span>
              {{ detail }}
            </li>
          </ul>
        </div>
      </li>
    </transition-group>
  </section>
</template>

<script setup>
const jobs = [
  {
    title: "Cloud/DeVops Engineer",
    company: "MojoPay",
    location: "Ghana",
    dates: "January 2022 – Present",
    details: [
      "Designed and implemented CI/CD pipelines in Jenkins for in-house applications, integrating automated testing and deployment processes.",
      "Managed DNS for MojoPay domains and services, ensuring availability, performance, and compliance.",
      "Developed automated scripts to streamline deployments, system maintenance, and operational workflows.",
      "Administered and optimized web servers (Nginx, HAProxy, IIS) for performance, security, and reliability.",
      "Managed and monitored Linux and Windows servers, ensuring stability and timely updates.",
      "Configured and maintained monitoring systems using Zabbix for proactive incident detection and resolution.",
      "Collaborated with development teams to align infrastructure with application requirements, enabling rapid and stable releases.",
      "Managed containerized workloads using Amazon ECS, including orchestration, scaling, and lifecycle management.",
      "Designed, implemented, and maintained AWS infrastructure following best practices for scalability, security, and high availability.",
      "Documented infrastructure, processes, and runbooks to ensure operational continuity and knowledge transfer.",
      "Troubleshot and resolved production incidents, focusing on root cause analysis and prevention.",
      "Implemented cloud security controls (IAM policies, network segmentation, encryption, WAF, GuardDuty) and ensured PCI DSS and SOC 2 compliance.",
    ]
  },
  {
    title: "DeVops Engineer",
    company: "Pragmatic Digital",
    location: "Leeds, United Kingdom",
    dates: "January 2021 – December 2022",
    details: [
      "Set up and maintained CI/CD pipelines using Jenkins and GitLab CI to streamline application builds, testing, and deployments.",
      "Managed AWS infrastructure including EC2, SQS, and related services to support high-availability applications",
      "Containerized and deployed applications using Docker, ensuring consistency across environments.",
      "Configured and secured Linux web servers for optimal performance and reliability.",
      "Mangged DNS for multiple domains, ensuring high availability and performance.",
      "Administered and optimized web servers (Nginx, HAProxy, IIS) for performance, security, and reliability."
    ]
  },
  {
    title: "Full Stack Software Engineer",
    company: "Pragmatic Digital",
    location: "Leeds, United Kingdom",
    dates: "May 2019 – January 2021",
    details: [
      "Built custom web applications using Python, JavaScript, and Vue.js",
      "Developed event-driven systems and performed web scraping with Python",
      "Built customs WordPress templates and custom plugins",
      "Integrated payment systems (Stripe, GoCardless) and third-party APIs (Algolia, Sage)",
      "Web Scraping with Python",
      "Developed and maintained RESTful APIs for frontend-backend communication",

      
      
    ]
  },
  {
    title: "Software Developer",
    company: "Supertech Ghana Limited",
    location: "Accra, Ghana",
    dates: "February 2018 – January 2019",
    details: [
      "Built applications using Java Spring and Laravel frameworks",
      "Designed and implemented database systems using PostgreSQL and MySQL",
      "Participated in Agile development (daily stand-ups, sprint planning)",
      "Created software design artifacts (use-case diagrams, activity diagrams)",
      "Set up LEMP stacks and developed on Ubuntu environments",
      "Collaborated via Git version control"
    ]
  },
  {
    title: "Software Engineer (VAS and Mobility)",
    company: "Information Technology Engineers",
    location: "Accra, Ghana",
    dates: "April 2017 – January 2018",
    details: [
      "Developed USSD applications and mobile apps using Apache Cordova",
      "Built web applications using PHP (CodeIgniter framework)",
      "Integrated third-party APIs and deployed applications on Windows Server 2012",
      "Practiced Agile methodology and used Git for source control",
      "Deployed and configured Linux-based web servers (LEMP stack)"
    ]
  },
  {
    title: "Software Engineer",
    company: "Nalo Solutions Limited",
    location: "Accra, Ghana",
    dates: "June 2016 – April 2017",
    details: [
      "Developed web apps using PHP Laravel and mobile apps using Apache Cordova",
      "Integrated USSD and third-party APIs for telecom and fintech platforms",
      "Set up and maintained Ubuntu web servers for hosting applications",
      "Diagnosed and resolved issues with SMS platforms",
      "Provided IT support: hardware setup, troubleshooting, and user assistance",
      "Maintained helpdesk systems and handled network issues",
      "Configured LEMP environments for deployment"
    ]
  }
];
</script>
<style scoped>
:root {
  --primary: #2563eb;
  --accent: #38bdf8;
  --bg-glass: rgba(255,255,255,0.85);
  --shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.18);
  --font-main: 'Inter', 'Segoe UI', Arial, sans-serif;
  --gradient: linear-gradient(135deg, #38bdf8 0%, #2563eb 100%);
}

.experience {
  padding: 3rem 1.5rem;
  background: var(--gradient);
  min-height: 100vh;
  max-width: 950px;
  margin: 0 auto;
  font-family: var(--font-main);
  position: relative;
  z-index: 1;
  border-radius: 2rem;
  box-shadow: 0 16px 40px 0 rgba(31, 38, 135, 0.10);
  overflow: hidden;
}

.experience::before {
  content: "";
  position: absolute;
  top: -80px; left: -80px;
  width: 300px; height: 300px;
  background: radial-gradient(circle, #38bdf8 40%, transparent 70%);
  opacity: 0.3;
  z-index: 0;
  animation: float 8s infinite alternate;
}
@keyframes float {
  0% { transform: translateY(0);}
  100% { transform: translateY(40px);}
}

h2 {
  font-size: 2.7rem;
  font-weight: 800;
  color: #2563eb;
  margin-bottom: 2.5rem;
  display: flex;
  align-items: center;
  gap: 1rem;
  letter-spacing: 0.03em;
  text-shadow: 0 2px 12px rgba(56,189,248,0.18);
  position: relative;
  z-index: 2;
}
h2::before {
  content: "";
  position: absolute;
  left: -1rem;
  top: 50%;
  transform: translateY(-50%);
  width: 100%;
  height: 3.5rem;
  background: rgba(255,255,255,0.22);
  filter: blur(8px);
  border-radius: 1rem;
  z-index: -1;
}

h2 {
  text-shadow:
    0 2px 12px rgba(56,189,248,0.25),
    0 0 0.5rem #fff,
    0 0 1.5rem #2563eb;
}

.icon-briefcase {
  display: inline-block;
  width: 2.5rem;
  height: 2.5rem;
  background: url('https://cdn.jsdelivr.net/npm/@tabler/icons/icons/briefcase.svg') no-repeat center/contain;
  filter: drop-shadow(0 2px 8px #38bdf8aa);
}

.job-list {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2.5rem;
  padding: 0;
  margin: 0;
}

@media (min-width: 700px) {
  .job-list {
    grid-template-columns: 1fr 1fr;
  }
}

.job-item {
  list-style: none;
}

.job-card {
  background: var(--bg-glass);
  border-radius: 1.5rem;
  box-shadow: 0 12px 32px 0 rgba(56,189,248,0.15), var(--shadow);
  padding: 2.2rem 1.7rem;
  backdrop-filter: blur(16px) saturate(120%);
  border: 1.5px solid #38bdf8;
  transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
  position: relative;
  overflow: hidden;
  z-index: 1;
}

.job-card::before {
  content: "";
  position: absolute;
  top: -40px; right: -40px;
  width: 120px; height: 120px;
  background: radial-gradient(circle, #2563eb 40%, transparent 70%);
  opacity: 0.12;
  z-index: 0;
}

.job-card:hover {
  transform: translateY(-10px) scale(1.03);
  box-shadow: 0 24px 60px 0 rgba(56,189,248,0.18), 0 8px 32px 0 rgba(31, 38, 135, 0.22);
  border-color: #2563eb;
}

.job-header {
  display: flex;
  align-items: flex-start;
  gap: 1.2rem;
  margin-bottom: 1.4rem;
}

.icon-company {
  width: 2.5rem;
  height: 2.5rem;
  background: url('https://cdn.jsdelivr.net/npm/@tabler/icons/icons/building.svg') no-repeat center/contain;
  flex-shrink: 0;
  opacity: 0.9;
  filter: drop-shadow(0 2px 8px #2563eb88);
}

.job-title {
  font-size: 1.3rem;
  color: var(--primary);
  font-weight: 700;
  margin-bottom: 0.2rem;
  letter-spacing: 0.01em;
}

.job-company {
  font-size: 1.05rem;
  color: #334155;
  font-weight: 600;
}

.job-location {
  color: var(--accent);
  font-size: 1rem;
  font-weight: 500;
}
.job-dates {
  font-size: 1rem;
  color: #64748b;
  margin-top: 0.2rem;
}

.job-details {
  margin-top: 1.4rem;
  padding-left: 0;
  list-style: none;
}

.job-details li {
  display: flex;
  align-items: flex-start;
  gap: 0.8rem;
  margin-bottom: 0.8rem;
  font-size: 1.05rem;
  color: #374151;
  line-height: 1.6;
  position: relative;
  font-family: var(--font-main);
}

.icon-dot {
  width: 0.8rem;
  height: 0.8rem;
  background: var(--accent);
  border-radius: 50%;
  margin-top: 0.45rem;
  flex-shrink: 0;
  box-shadow: 0 2px 6px #38bdf844;
  border: 2px solid #fff;
}
/* Animation: fade in with slide-up */
.fade-stagger-enter-active {
  transition: all 0.6s cubic-bezier(.4,0,.2,1);
}
.fade-stagger-leave-active {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.3s cubic-bezier(.4,0,.2,1);
}
.fade-stagger-enter-from {
  opacity: 0;
  transform: translateY(20px);
}
.fade-stagger-enter-to {
  opacity: 1;
  transform: translateY(0);
}

/* Modern scrollbar */
.experience::-webkit-scrollbar {
  width: 8px;
  background: transparent;
}
.experience::-webkit-scrollbar-thumb {
  background: var(--accent);
  border-radius: 8px;
  opacity: 0.5;
}

@media (max-width: 600px) {
  .experience {
    padding: 1.2rem 0.5rem;
    font-size: 1rem;
  }
  h2 {
    font-size: 1.5rem;
  }
  .job-card {
    padding: 1rem 0.5rem;
  }
  .job-title {
    font-size: 1rem;
  }
  .job-company,
  .job-location,
  .job-dates {
    font-size: 0.95rem;
  }
  .job-details li {
    font-size: 0.98rem;
  }
}
</style>

