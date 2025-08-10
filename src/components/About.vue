<template>
  <section class="about">
    <h2>About Me</h2>

    <p>
      I am a <strong>results-driven Cloud Software Engineer</strong> with over <strong>8 years of industry experience</strong>, 
      specializing in <strong>DevOps</strong>, <strong>full-stack web development</strong>, and 
      <strong>Cloud architecting</strong>. My core strengths lie in architecting <strong>secure, scalable cloud infrastructure</strong> 
      on AWS, Azure, and Google Cloud, with deep expertise in <strong>automation</strong>, 
      <em>Infrastructure as Code (IaC)</em>, and compliance frameworks such as <strong>PCI DSS</strong> and <strong>ISO 270001</strong>.
    </p>

    <p>
      With a solid foundation in <strong>CI/CD pipelines using Jenkins</strong>, container orchestration (ECS, EKS, Docker), 
      and <strong>cloud security best practices</strong>, I build <strong>resilient systems</strong> that meet both agility and regulatory requirements. 
      I simplify operations through <strong>smart tooling</strong>, automation at scale, and <em>well-maintained documentation</em>.
    </p>

    <p>
      As an <strong>AWS-certified solutions Architect</strong> with a <strong>BSc in Computer Science and Engineering</strong>, 
      I bring hands-on experience as a <strong>full-stack software developer</strong> — delivering performant applications using <strong>Laravel</strong> and <strong>Vue.js including other programming languages</strong>. 
      This hybrid skill set enables me to bridge the gap between <strong>infrastructure and application development teams</strong> effectively.
    </p>

    <p>
      Throughout my career, I’ve contributed to <strong>large-scale delivery teams</strong>, implementing strategic initiatives, 
      resolving client-facing challenges, and driving value through <strong>continuous process improvement</strong> and <strong>automation</strong>.
    </p>
  </section>
</template>



<style scoped>
.about {
  font-family: 'Inter', 'Segoe UI', Arial, sans-serif;
  line-height: 1.85;
  font-size: 1.18rem;
  color: #22223b;
  max-width: 850px;
  margin: 2.5rem auto;
  padding: 2.5rem 2rem;
  background: rgba(255,255,255,0.85);
  border-radius: 1.5rem;
  box-shadow: 0 8px 32px 0 rgba(56,189,248,0.12), 0 2px 8px 0 rgba(31,38,135,0.08);
  backdrop-filter: blur(12px) saturate(120%);
  border: 1.5px solid #38bdf8;
  position: relative;
  z-index: 1;
}
.about::before {
  content: "";
  position: absolute;
  top: -60px; left: -60px;
  width: 220px; height: 220px;
  background: radial-gradient(circle, #38bdf8 40%, transparent 70%);
  opacity: 0.18;
  z-index: 0;
  animation: float 7s infinite alternate;
}
@keyframes float {
  0% { transform: translateY(0);}
  100% { transform: translateY(30px);}
}

.about h2 {
  font-size: 2.6rem;
  margin-bottom: 2rem;
  color: #2563eb;
  font-weight: 800;
  letter-spacing: 0.03em;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  border-bottom: none;
  padding-bottom: 0;
  text-shadow: 0 2px 12px rgba(56,189,248,0.13);
}

.about strong {
  color: #2563eb;
  font-weight: 700;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.about em {
  font-style: italic;
  color: #d63384;
  font-weight: 600;
  background: linear-gradient(90deg, #d63384 0%, #38bdf8 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.about p {
  margin-bottom: 1.5rem;
  background: rgba(255,255,255,0.6);
  border-radius: 0.7rem;
  padding: 1.1rem 1rem;
  box-shadow: 0 2px 8px rgba(56,189,248,0.07);
  transition: box-shadow 0.2s;
  position: relative;
  z-index: 1;
}

.about p:hover {
  box-shadow: 0 8px 24px rgba(56,189,248,0.13);
}

@media (max-width: 600px) {
  .about {
    padding: 1.2rem 0.5rem;
    font-size: 1rem;
  }
  .about h2 {
    font-size: 2rem;
  }
  .about p {
    padding: 0.8rem 0.5rem;
  }
}
</style>