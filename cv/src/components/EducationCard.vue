<template>
  <div class="education-card">
    <h3>{{ title }}</h3>
    <p class="institution">{{ institution }}</p>
    <p v-if="status" class="status">{{ status }}</p>
  </div>
</template>

<script setup lang="ts">
interface Props {
  title: string;
  institution: string;
  status?: string;
}

defineProps<Props>();
</script>

<style scoped>
.education-card {
  background: white;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  margin-bottom: 1rem;
  transition: transform 0.3s ease;
}

.education-card:hover {
  transform: translateX(5px);
}

.education-card h3 {
  color: #333;
  margin-bottom: 0.5rem;
}

.institution {
  color: #667eea;
  font-weight: 600;
  margin-bottom: 0.25rem;
}

.status {
  color: #666;
  font-style: italic;
}
</style>
