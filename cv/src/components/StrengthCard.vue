<template>
  <div class="strength-card">
    <div class="strength-icon">{{ icon }}</div>
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
.strength-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: all 0.3s ease;
}

.strength-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}

.strength-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.strength-card h3 {
  color: #667eea;
  margin-bottom: 0.5rem;
}

.strength-card p {
  color: #666;
  line-height: 1.6;
}
</style>
