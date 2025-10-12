<template>
  <a v-if="href" :href="href" class="contact-card">
    <div class="contact-icon">{{ icon }}</div>
    <h3>{{ title }}</h3>
    <p>{{ content }}</p>
  </a>
  <div v-else class="contact-card">
    <div class="contact-icon">{{ icon }}</div>
    <h3>{{ title }}</h3>
    <p>{{ content }}</p>
  </div>
</template>

<script setup lang="ts">
interface Props {
  icon: string;
  title: string;
  content: string;
  href?: string;
}

defineProps<Props>();
</script>

<style scoped>
.contact-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: all 0.3s ease;
  text-decoration: none;
  color: inherit;
  animation: fadeInUp 0.8s ease-out;
  display: block;
}

.contact-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.contact-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.contact-card h3 {
  color: #667eea;
  margin-bottom: 0.5rem;
  font-size: 1.3rem;
}

.contact-card p {
  color: #333;
  word-break: break-word;
  font-size: 1.1rem;
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
</style>
