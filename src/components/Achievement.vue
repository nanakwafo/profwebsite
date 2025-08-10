<template>
  <section class="achievement">
    <h2>
      <span class="icon-trophy">🏆</span>
      Key Achievements
    </h2>
    <div class="achievement-list">
      <transition-group name="fade-stagger" tag="div">
        <div class="achievement-card" key="mojopay-network">
          <div class="card-header">
            <span class="icon-achieve">🌐</span>
            <h3>Secure & Compliant AWS Network for MojoPay</h3>
          </div>
          <ul class="achievement-details">
            <li>
              <strong>Situation:</strong>
              MojoPay, a payment solutions provider, needed a secure, scalable, and highly available cloud network to host its payment processing platform while meeting strict PCI DSS compliance requirements.
            </li>
            <li>
              <strong>Task:</strong>
              As AWS Solutions Architect, I was responsible for designing and implementing a cloud network architecture that ensured security, compliance, and performance for the payment platform.
            </li>
            <li>
              <strong>Action:</strong>
              <ul>
                <li>Designed a multi-tier AWS VPC architecture with private/public subnets, NAT gateways, and load balancers to isolate sensitive payment data.</li>
                <li>Implemented network segmentation, security groups, and network ACLs to enforce PCI DSS security controls.</li>
                <li>Deployed AWS WAF and AWS Network Firewall to protect against web exploits and unauthorized access.</li>
                <li>Configured CloudWatch logging, VPC Flow Logs, and GuardDuty for continuous monitoring and threat detection.</li>
              </ul>
            </li>
            <li>
              <strong>Result:</strong>
              Delivered a secure, compliant, and high-performance cloud network that supported MojoPay’s payment platform operations and successfully passed PCI DSS certification audits.
            </li>
          </ul>
        </div>
        <div class="divider" key="divider0"></div>
        <div class="achievement-card" key="mojopay">
          <div class="card-header">
            <span class="icon-achieve">🔒</span>
            <h3>PCI DSS Certification for MojoPay</h3>
          </div>
          <ul class="achievement-details">
            <li>
              <strong>Situation:</strong>
              MojoPay, a payment solutions provider, needed to achieve PCI DSS certification to meet regulatory requirements and build client trust.
            </li>
            <li>
              <strong>Task:</strong>
              As AWS Solutions Architect and PCI DSS Compliance Officer, I was responsible for designing a secure, compliant cloud infrastructure and leading the organization through the full certification process.
            </li>
            <li>
              <strong>Action:</strong>
              <ul>
                <li>Architected and implemented a PCI DSS-compliant AWS environment leveraging security best practices, network segmentation, and encryption controls.</li>
                <li>Developed and enforced policies, procedures, and documentation to meet PCI DSS audit requirements.</li>
                <li>Coordinated with internal teams, QSA auditors, and third-party vendors to close compliance gaps.</li>
                <li>Automated security monitoring, logging, and vulnerability scanning to maintain continuous compliance.</li>
              </ul>
            </li>
            <li>
              <strong>Result:</strong>
              Achieved full PCI DSS certification on schedule, enabling MojoPay to securely process card payments, win new merchant partnerships, and enhance its market credibility.
            </li>
          </ul>
        </div>
        <div class="divider" key="divider1"></div>
        <div class="achievement-card" key="mojopay-cicd">
          <div class="card-header">
            <span class="icon-achieve">⚙️</span>
            <h3>Automated CI/CD Pipeline for MojoPay</h3>
          </div>
          <ul class="achievement-details">
            <li>
              <strong>Situation:</strong>
              Deployment of new application features at MojoPay was slow, error-prone, and required significant manual intervention, delaying releases and increasing downtime risk.
            </li>
            <li>
              <strong>Task:</strong>
              As the DevOps/SRE lead, I was responsible for designing and implementing an automated CI/CD pipeline to streamline the build, test, and deployment process while ensuring compliance with security and regulatory requirements.
            </li>
            <li>
              <strong>Action:</strong>
              <ul>
                <li>Designed and built a Jenkins-based CI/CD pipeline integrating Git, Docker, and AWS ECS for containerized deployments.</li>
                <li>Implemented automated testing, static code analysis, and security scanning (Snyk, Trivy) as part of the pipeline to ensure high code quality and PCI DSS compliance.</li>
                <li>Introduced parallel build stages and environment-specific deployment jobs to optimize speed and reliability.</li>
                <li>Automated infrastructure provisioning with Terraform and configuration management via Ansible for consistent, repeatable environments.</li>
              </ul>
            </li>
            <li>
              <strong>Result:</strong>
              Reduced deployment time from 1 hour to under 10 minutes, enabled zero-downtime releases, and improved release frequency by 50%, significantly enhancing development agility and production stability.
            </li>
          </ul>
        </div>
        <div class="divider" key="divider2"></div>
        <div class="achievement-card" key="swoove">
          <div class="card-header">
            <span class="icon-achieve">🚚</span>
            <h3>Swoove Delivery Plugin for WooCommerce</h3>
          </div>
          <ul class="achievement-details">
            <li>
              <strong>Situation:</strong>
              Swoove 360, a logistics and delivery solutions provider, needed a seamless way to integrate its services into WooCommerce-powered eCommerce sites to streamline order fulfillment.
            </li>
            <li>
              <strong>Task:</strong>
              As the sole developer, I was tasked with creating a custom WordPress plugin that could automate and optimize delivery workflows.
            </li>
            <li>
              <strong>Action:</strong>
              <ul>
                <li>Designed, developed, and deployed the Swoove Delivery plugin for WordPress from scratch.</li>
                <li>Integrated real-time order tracking, automated delivery scheduling, and logistics management directly into WooCommerce stores.</li>
                <li>Implemented secure API communication between WooCommerce and Swoove’s logistics platform.</li>
                <li>Published and maintained the plugin on the WordPress Plugin Directory: <a href="https://wordpress.org/plugins/swoove-delivery/">Swoove Delivery.</a></li>
              </ul>
            </li>
            <li>
              <strong>Result:</strong>
              Improved delivery efficiency and logistics coordination for multiple eCommerce businesses, reducing manual processing time and enhancing customer satisfaction.
            </li>
          </ul>
        </div>
      </transition-group>
    </div>
  </section>
  </template>
<style scoped>
.achievement {
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

.achievement::before {
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
  display: flex;
  align-items: center;
  gap: 0.7rem;
  text-shadow: 0 2px 12px rgba(56,189,248,0.13);
}

.icon-trophy {
  font-size: 2rem;
  margin-right: 0.5rem;
}

.achievement-list {
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
}

.achievement-card {
  background: rgba(255,255,255,0.85);
  border-radius: 1.1rem;
  box-shadow: 0 4px 16px rgba(56,189,248,0.10);
  padding: 2rem 1.5rem;
  position: relative;
  z-index: 1;
  transition: box-shadow 0.25s, transform 0.25s;
  animation: fadeInUp 0.8s;
}

.achievement-card:hover {
  box-shadow: 0 12px 32px rgba(56,189,248,0.15), 0 2px 8px rgba(31,38,135,0.13);
  transform: translateY(-6px) scale(1.01);
}

@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px);}
  to { opacity: 1; transform: translateY(0);}
}

.card-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.2rem;
}

.icon-achieve {
  font-size: 2rem;
  filter: drop-shadow(0 2px 8px #38bdf8aa);
}

.achievement-card h3 {
  font-size: 1.3rem;
  color: #2563eb;
  font-weight: 700;
  margin-bottom: 0.2rem;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.achievement-details {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 1.08rem;
  color: #374151;
  line-height: 1.7;
}

.achievement-details > li {
  margin-bottom: 1.2rem;
  background: rgba(255,255,255,0.6);
  border-radius: 0.7rem;
  padding: 1rem 1rem 0.7rem 1rem;
  box-shadow: 0 2px 8px rgba(56,189,248,0.07);
}

.achievement-details strong {
  color: #2563eb;
  font-weight: 700;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.achievement-details ul {
  margin-top: 0.7rem;
  margin-bottom: 0.7rem;
  padding-left: 1.2rem;
}

.achievement-details ul li {
  margin-bottom: 0.5rem;
  font-size: 1rem;
  color: #374151;
  background: none;
  border-radius: 0;
  padding: 0;
  box-shadow: none;
}

.divider {
  height: 2px;
  background: linear-gradient(90deg, #38bdf8 0%, #2563eb 100%);
  border-radius: 1px;
  margin: 0 0 0 0;
  opacity: 0.18;
}

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
  .achievement {
    padding: 1.2rem 0.5rem;
    font-size: 1rem;
  }
  h2 {
    font-size: 1.5rem;
  }
  .achievement-list {
    gap: 1.5rem;
  }
  .achievement-card {
    padding: 1rem 0.5rem;
  }
  .achievement-card h3 {
    font-size: 1.1rem;
  }
  .achievement-details > li {
    padding: 0.7rem 0.5rem 0.5rem 0.5rem;
    font-size: 0.98rem;
  }
}
</style>