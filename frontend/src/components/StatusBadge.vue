<script setup lang="ts">
defineProps<{
  status: 'APPLIED' | 'INTERVIEW' | 'OFFER' | 'ACCEPTED' | 'REJECTED'
}>()
</script>

<template>
  <span class="badge" :class="status.toLowerCase()">{{ status }}</span>
</template>

<style scoped>
.badge {
  display: inline-block;
  padding: 0.1rem 0.5rem;
  border-radius: 999px;
  font-size: 0.75rem;
  font-weight: 600;
  background: #e4e7eb;
}

.interview {
  background: #fff3c4;
}

.offer {
  background: #d9e8ff;
}

.accepted {
  background: #d3f4dc;
}

.rejected {
  background: #fde2e2;
}
</style>
