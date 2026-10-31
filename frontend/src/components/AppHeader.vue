<script setup lang="ts">
// Static for now: the role and links will come from the auth store at Check 5.
defineProps<{
  role: 'STUDENT' | 'ADVISOR'
}>()
</script>

<template>
  <header class="app-header">
    <strong>Internship Tracker</strong>
    <nav>
      <a v-if="role === 'STUDENT'" href="#">My applications</a>
      <a v-else href="#">Students' applications</a>
      <a href="#">Profile</a>
      <button class="btn" type="button">Log out</button>
    </nav>
  </header>
</template>

<style scoped>
.app-header {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  gap: 0.75rem;
  padding: 0.75rem 1rem;
  background: var(--color-surface);
  border-bottom: 1px solid var(--color-border);
}

nav {
  display: flex;
  align-items: center;
  gap: 1rem;
}
</style>
