<template>
  <div class="highlight-card">
    <div class="icon">{{ icon }}</div>
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
  </div>
</template>

<script setup lang="ts">
interface Props {
  icon: string;
  title: string;
  description: string;
}

defineProps<Props>();
</script>

<style scoped>
.highlight-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  text-align: center;
  animation: fadeInUp 1s ease-out;
}

.highlight-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.15);
}

.icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.highlight-card h3 {
  color: #667eea;
  margin-bottom: 0.5rem;
  font-size: 1.5rem;
}

.highlight-card p {
  color: #666;
  line-height: 1.6;
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
