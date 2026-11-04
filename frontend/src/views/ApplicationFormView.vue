<script setup lang="ts">
import AppHeader from '../components/AppHeader.vue'
</script>

<template>
  <AppHeader role="STUDENT" />
  <main class="page">
    <form class="card" @submit.prevent>
      <h1>Add application</h1>
      <div class="field">
        <label for="company">Company</label>
        <input id="company" type="text" />
        <span class="error">Company is required</span>
      </div>
      <div class="field">
        <label for="position">Position</label>
        <input id="position" type="text" />
        <span class="error">Position is required</span>
      </div>
      <div class="field">
        <label for="appliedAt">Date applied</label>
        <input id="appliedAt" type="date" />
        <span class="error">Date applied cannot be in the future</span>
      </div>
      <div class="field">
        <label for="notes">Notes</label>
        <textarea id="notes" rows="3"></textarea>
      </div>
      <div class="field">
        <label for="cv">CV (PDF)</label>
        <input id="cv" type="file" accept="application/pdf" />
        <span class="hint">PDF only, 2 MB or smaller</span>
      </div>
      <div class="actions">
        <button class="btn" type="button">Cancel</button>
        <button class="btn btn-primary" type="submit">Save</button>
      </div>
    </form>
  </main>
</template>
