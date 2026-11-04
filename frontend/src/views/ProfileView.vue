<script setup lang="ts">
import AppHeader from '../components/AppHeader.vue'
</script>

<template>
  <AppHeader role="STUDENT" />
  <main class="page">
    <section class="card">
      <h1>Profile</h1>
      <dl>
        <dt>Name</dt>
        <dd>PUM Brusmuny</dd>
        <dt>Email</dt>
        <dd>student@example.com</dd>
        <dt>Role</dt>
        <dd>Student</dd>
        <dt>Advisor</dt>
        <dd>Mr. Advisor</dd>
      </dl>
    </section>
  </main>
</template>

<style scoped>
dl {
  display: grid;
  grid-template-columns: max-content 1fr;
  gap: 0.5rem 1.5rem;
  margin: 0;
}

dt {
  font-weight: 600;
}

dd {
  margin: 0;
}
</style>
