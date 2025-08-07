<template>
  <section class="experience">
    <h2>Experience</h2>
    <transition-group name="fade-stagger" tag="ul" class="job-list">
      <li v-for="(job, index) in jobs" :key="index" class="job-item">
        <strong class="job-title">
          {{ job.title }}<br />
          <span class="job-company">{{ job.company }}, {{ job.location }}</span><br />
          <span class="job-dates">{{ job.dates }}</span>
        </strong>
        <ul class="job-details">
          <li v-for="(detail, i) in job.details" :key="i">{{ detail }}</li>
        </ul>
      </li>
    </transition-group>
  </section>
</template>

<script setup>
const jobs = [
  {
    title: "DeVops Engineer",
    company: "MojoPay",
    location: "Ghana",
    dates: "January 2022 – Present",
    details: [
      "Built custom web applications using Python, JavaScript, and Vue.js",
      "Developed event-driven systems and performed web scraping with Python",
      "Built WordPress templates and custom plugins",
      "Integrated payment systems (Stripe, GoCardless) and third-party APIs (Algolia, Sage)",
      "Set up and maintained CI/CD pipelines using Jenkins and GitLab CI",
      "Managed AWS infrastructure (EC2, SQS, etc.) and containerized apps with Docker",
      "Configured Linux web servers and deployed applications securely"
    ]
  },
  {
    title: "Full Stack Software Engineer",
    company: "Pragmatic Digital",
    location: "Leeds, United Kingdom",
    dates: "May 2020 – January 2022",
    details: [
      "Built custom web applications using Python, JavaScript, and Vue.js",
      "Developed event-driven systems and performed web scraping with Python",
      "Built WordPress templates and custom plugins",
      "Integrated payment systems (Stripe, GoCardless) and third-party APIs (Algolia, Sage)",
      "Set up and maintained CI/CD pipelines using Jenkins and GitLab CI",
      "Managed AWS infrastructure (EC2, SQS, etc.) and containerized apps with Docker",
      "Configured Linux web servers and deployed applications securely"
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
.experience {
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

.job-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.job-item {
  background: #fff;
  border-left: 4px solid #1a73e8;
  padding: 1.2rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
  border-radius: 6px;
  transition: all 0.3s ease;
}

.job-title {
  font-size: 1.1rem;
  color: #1f2937;
}

.job-company {
  font-weight: normal;
  color: #555;
}

.job-dates {
  font-size: 0.9rem;
  color: #888;
}

.job-details {
  list-style: disc;
  padding-left: 1.2rem;
  margin-top: 0.8rem;
  color: #444;
}

.job-details li {
  margin-bottom: 0.4rem;
}

/* Animation: fade in with slide-up */
.fade-stagger-enter-active {
  transition: all 0.6s ease;
}
.fade-stagger-leave-active {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.3s ease;
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

