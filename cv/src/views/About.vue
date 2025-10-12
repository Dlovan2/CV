<template>
  <div class="about">
    <div class="about-header">
      <h1>About Me</h1>
      <p class="tagline">Software Engineer | Problem Solver | Team Player</p>
    </div>

    <div class="content-wrapper">
      <section class="info-section">
        <h2>Personal Information</h2>
        <div class="info-grid">
          <div class="info-item">
            <strong>Full Name:</strong>
            <span>Dlovan Faysal Ahmad</span>
          </div>
          <div class="info-item">
            <strong>Location:</strong>
            <span>Erbil, Braiaty</span>
          </div>
          <div class="info-item">
            <strong>Phone:</strong>
            <span>07503889591</span>
          </div>
          <div class="info-item">
            <strong>Email:</strong>
            <span>dlovanfaisal180@gmail.com</span>
          </div>
        </div>
      </section>

      <section class="info-section">
        <h2>Education</h2>
        <EducationCard
          title="B.Sc. in Software Engineering"
          institution="Salahaddin University, Erbil"
          status="Currently in 4th Year"
        />
        <EducationCard
          title="High School Graduate"
          institution="Rozak School"
        />
      </section>

      <section class="info-section">
        <h2>Core Strengths</h2>
        <div class="strengths-grid">
          <StrengthCard
            icon="🧩"
            title="Problem Solving"
            description="Excellent analytical abilities and creative solution development"
          />
          <StrengthCard
            icon="🤝"
            title="Teamwork"
            description="Strong interpersonal skills and effective group collaboration"
          />
          <StrengthCard
            icon="⚡"
            title="Adaptability"
            description="Quick learner, able to acquire new skills as needed"
          />
          <StrengthCard
            icon="💬"
            title="Communication"
            description="Clear and effective communication in multicultural settings"
          />
        </div>
      </section>

      <section class="info-section">
        <h2>Language Skills</h2>
        <div class="languages">
          <div class="language-badge">Kurdish (Native)</div>
          <div class="language-badge">Arabic (Fluent)</div>
          <div class="language-badge">English (Fluent)</div>
        </div>
        <p class="language-note">Trilingual communication enables seamless interaction in multicultural environments</p>
      </section>
    </div>
  </div>
</template>

<script setup lang="ts">
import EducationCard from '../components/EducationCard.vue';
import StrengthCard from '../components/StrengthCard.vue';
</script>

<style scoped>
.about {
  min-height: 100vh;
  padding-bottom: 4rem;
}

.about-header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 4rem 2rem;
  text-align: center;
}

.about-header h1 {
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

.info-section {
  margin-bottom: 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.info-section h2 {
  color: #667eea;
  font-size: 2rem;
  margin-bottom: 1.5rem;
  border-bottom: 3px solid #667eea;
  padding-bottom: 0.5rem;
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
}

.info-item {
  background: white;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.info-item:hover {
  transform: translateY(-3px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.info-item strong {
  color: #667eea;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.info-item span {
  color: #333;
  font-size: 1.1rem;
}

.strengths-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}

.languages {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  margin-bottom: 1rem;
}

.language-badge {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 0.75rem 1.5rem;
  border-radius: 25px;
  font-weight: 600;
  transition: transform 0.3s ease;
}

.language-badge:hover {
  transform: scale(1.05);
}

.language-note {
  color: #666;
  font-style: italic;
  margin-top: 1rem;
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

@media (max-width: 768px) {
  .about-header h1 {
    font-size: 2rem;
  }

  .tagline {
    font-size: 1.1rem;
  }

  .info-section h2 {
    font-size: 1.5rem;
  }
}
</style>
