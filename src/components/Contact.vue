<template>
  <section>
    <h2>Contact</h2>
    <p>Email: <a href="mailto:nanamensah1140@gmail.com">nanamensah1140@gmail.com</a></p>
    <p>Phone: +233 598 296 977</p>
    <p>GitHub: <a href="https://github.com/nanamensah" target="_blank">github.com/nanamensah</a></p>
    <p>LinkedIn: <a href="https://linkedin.com/in/nanamensah" target="_blank">linkedin.com/in/nanamensah</a></p>
  </section>
</template>

<style scoped>
section {
  padding: 2.5rem 1.5rem;
  max-width: 600px;
  margin: 2.5rem auto;
  background: linear-gradient(135deg, #e0e7ff 0%, #f0fdfa 100%);
  border-radius: 1.5rem;
  box-shadow: 0 8px 32px 0 rgba(56,189,248,0.10), 0 2px 8px 0 rgba(31,38,135,0.08);
  font-family: 'Inter', 'Segoe UI', Arial, sans-serif;
  position: relative;
  z-index: 1;
  overflow: hidden;
}

section::before {
  content: "";
  position: absolute;
  top: -60px; left: -60px;
  width: 180px; height: 180px;
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
  font-size: 2.1rem;
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

p {
  font-size: 1.13rem;
  color: #374151;
  margin-bottom: 1.2rem;
  background: rgba(255,255,255,0.7);
  border-radius: 0.7rem;
  padding: 0.8rem 1rem;
  box-shadow: 0 2px 8px rgba(56,189,248,0.07);
  display: flex;
  align-items: center;
  gap: 0.7rem;
}

a {
  color: #2563eb;
  font-weight: 600;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-decoration: none;
  transition: color 0.2s, text-shadow 0.2s;
  word-break: break-all;
}

a:hover {
  text-shadow: 0 2px 12px #38bdf855;
  color: #38bdf8;
  text-decoration: underline;
}

@media (max-width: 600px) {
  section {
    padding: 1.2rem 0.5rem;
    font-size: 1rem;
  }
  h2 {
    font-size: 1.3rem;
  }
  p {
    padding: 0.6rem 0.5rem;
    font-size: 1rem;
  }
}
</style>
