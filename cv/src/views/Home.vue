<template>
  <div class="home">
    <div class="hero">
      <div class="hero-content">
        <h1 class="name-title">Dlovan Faysal Ahmad</h1>
        <p class="subtitle">Software Engineering Student & Technology Enthusiast</p>
        <div class="hero-buttons">
          <router-link to="/about" class="btn btn-primary">Learn More About Me</router-link>
          <router-link to="/contact" class="btn btn-secondary">Get In Touch</router-link>
        </div>
      </div>
    </div>

    <section class="highlights">
      <HighlightCard
        icon="🎓"
        title="Education"
        description="4th Year Software Engineering Student at Salahaddin University"
      />
      <HighlightCard
        icon="💼"
        title="Experience"
        description="Diverse background in tech, sales, and operations"
      />
      <HighlightCard
        icon="🌍"
        title="Languages"
        description="Fluent in Kurdish, Arabic, and English"
      />
    </section>
  </div>
</template>

<script setup lang="ts">
import HighlightCard from '../components/HighlightCard.vue';
</script>

<style scoped>
.home {
  min-height: 100vh;
}

.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  min-height: 70vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
  padding: 2rem;
}

.hero-content {
  max-width: 800px;
  animation: fadeInUp 1s ease-out;
}

.name-title {
  font-size: 3.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
  animation: fadeInUp 1s ease-out 0.2s both;
}

.subtitle {
  font-size: 1.5rem;
  margin-bottom: 2rem;
  opacity: 0.95;
  animation: fadeInUp 1s ease-out 0.4s both;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
  animation: fadeInUp 1s ease-out 0.6s both;
}

.btn {
  padding: 0.875rem 2rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  display: inline-block;
}

.btn-primary {
  background: white;
  color: #667eea;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}

.btn-secondary {
  background: transparent;
  color: white;
  border: 2px solid white;
}

.btn-secondary:hover {
  background: white;
  color: #667eea;
  transform: translateY(-2px);
}

.highlights {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  padding: 4rem 2rem;
  max-width: 1200px;
  margin: 0 auto;
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
  .name-title {
    font-size: 2.5rem;
  }

  .subtitle {
    font-size: 1.2rem;
  }

  .hero-buttons {
    flex-direction: column;
  }

  .btn {
    width: 100%;
  }
}
</style>
