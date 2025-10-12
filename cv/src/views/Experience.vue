<template>
  <div class="experience">
    <div class="experience-header">
      <h1>Professional Experience</h1>
      <p class="tagline">Building skills through diverse roles in technology and service</p>
    </div>

    <div class="content-wrapper">
      <section class="work-section">
        <h2>Work History</h2>
        <div class="timeline">
          <div class="timeline-item" v-for="(job, index) in workExperience" :key="index">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>{{ job.title }}</h3>
              <p class="company">{{ job.company }}</p>
              <p class="duration">{{ job.duration }}</p>
              <p class="description">{{ job.description }}</p>
            </div>
          </div>
        </div>
      </section>

      <section class="certifications-section">
        <h2>Volunteering & Certifications</h2>
        <div class="certs-grid">
          <div class="cert-card">
            <div class="cert-icon">🎪</div>
            <h3>TEDx Nishtiman</h3>
            <p class="cert-title">Certified Management</p>
            <p class="cert-count">3 Events</p>
          </div>
          <div class="cert-card">
            <div class="cert-icon">🏢</div>
            <h3>Erbil International Fair</h3>
            <p class="cert-title">Certified Receptionist</p>
            <p class="cert-location">EIF Center</p>
          </div>
        </div>
      </section>

      <section class="skills-overview">
        <h2>Key Skills Developed</h2>
        <div class="skills-container">
          <div class="skill-tag" v-for="skill in skills" :key="skill">{{ skill }}</div>
        </div>
      </section>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface Job {
  title: string;
  company: string;
  duration: string;
  description: string;
}

const workExperience = ref<Job[]>([
  {
    title: 'Sales Representative & Computer Technician',
    company: 'IBM Touch',
    duration: '1 Year',
    description: 'Managed sales operations and provided technical support for computer systems, combining customer service with hands-on technical expertise.'
  },
  {
    title: 'CCTV Operative',
    company: 'Holland Bazaar',
    duration: '4 Months',
    description: 'Monitored security systems and maintained surveillance operations, ensuring safety and security protocols were followed.'
  },
  {
    title: 'Cashier',
    company: 'Samo',
    duration: '2 Months',
    description: 'Handled customer transactions, managed cash operations, and provided excellent customer service in a fast-paced retail environment.'
  }
]);

const skills = ref<string[]>([
  'Technical Support',
  'Customer Service',
  'Sales',
  'Security Operations',
  'Cash Handling',
  'Problem Solving',
  'Team Collaboration',
  'Communication',
  'Adaptability',
  'Time Management'
]);
</script>

<style scoped>
.experience {
  min-height: 100vh;
  padding-bottom: 4rem;
}

.experience-header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 4rem 2rem;
  text-align: center;
}

.experience-header h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  animation: fadeInUp 0.8s ease-out;
}

.tagline {
  font-size: 1.3rem;
  opacity: 0.95;
  animation: fadeInUp 0.8s ease-out 0.2s both;
}

.content-wrapper {
  max-width: 1000px;
  margin: 0 auto;
  padding: 3rem 2rem;
}

.work-section,
.certifications-section,
.skills-overview {
  margin-bottom: 3rem;
}

.work-section h2,
.certifications-section h2,
.skills-overview h2 {
  color: #667eea;
  font-size: 2rem;
  margin-bottom: 2rem;
  border-bottom: 3px solid #667eea;
  padding-bottom: 0.5rem;
  animation: fadeInUp 0.8s ease-out;
}

.timeline {
  position: relative;
  padding-left: 2rem;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 3px;
  background: linear-gradient(to bottom, #667eea, #764ba2);
}

.timeline-item {
  position: relative;
  padding-bottom: 2rem;
  animation: fadeInLeft 0.8s ease-out;
}

.timeline-marker {
  position: absolute;
  left: -2.5rem;
  top: 0;
  width: 1rem;
  height: 1rem;
  background: #667eea;
  border-radius: 50%;
  border: 3px solid white;
  box-shadow: 0 0 0 3px #667eea;
}

.timeline-content {
  background: white;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.timeline-content:hover {
  transform: translateX(5px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.timeline-content h3 {
  color: #333;
  margin-bottom: 0.5rem;
  font-size: 1.3rem;
}

.company {
  color: #667eea;
  font-weight: 600;
  margin-bottom: 0.25rem;
}

.duration {
  color: #999;
  font-size: 0.9rem;
  margin-bottom: 0.75rem;
}

.description {
  color: #666;
  line-height: 1.6;
}

.certs-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.cert-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: all 0.3s ease;
  animation: fadeInUp 0.8s ease-out;
}

.cert-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}

.cert-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.cert-card h3 {
  color: #667eea;
  margin-bottom: 0.5rem;
  font-size: 1.3rem;
}

.cert-title {
  color: #333;
  font-weight: 600;
  margin-bottom: 0.25rem;
}

.cert-count,
.cert-location {
  color: #666;
  font-size: 0.9rem;
}

.skills-container {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.skill-tag {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 0.75rem 1.5rem;
  border-radius: 25px;
  font-weight: 600;
  transition: all 0.3s ease;
  animation: fadeInUp 0.8s ease-out;
}

.skill-tag:hover {
  transform: scale(1.05) translateY(-2px);
  box-shadow: 0 4px 12px rgba(102, 126, 234, 0.4);
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (max-width: 768px) {
  .experience-header h1 {
    font-size: 2rem;
  }

  .tagline {
    font-size: 1.1rem;
  }

  .timeline {
    padding-left: 1.5rem;
  }

  .timeline-marker {
    left: -2rem;
  }
}
</style>
