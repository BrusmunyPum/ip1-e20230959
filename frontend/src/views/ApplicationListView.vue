<script setup lang="ts">
import AppHeader from '../components/AppHeader.vue'
import StatusBadge from '../components/StatusBadge.vue'

// Static sample rows for Check 1; they move to a Pinia store with mock data at Check 2.
const applications = [
  { id: 3, company: 'ABA Bank', position: 'Backend intern', appliedAt: '2026-10-18', status: 'INTERVIEW' },
  { id: 2, company: 'Smart Axiata', position: 'Frontend intern', appliedAt: '2026-10-12', status: 'APPLIED' },
  { id: 1, company: 'Wing Bank', position: 'QA intern', appliedAt: '2026-10-05', status: 'REJECTED' },
] as const
</script>

<template>
  <AppHeader role="STUDENT" />
  <main class="page">
    <div class="toolbar">
      <h1>My applications</h1>
      <button class="btn btn-primary" type="button">+ Add application</button>
    </div>
    <p class="hint">2 of 5 active applications</p>

    <div class="toolbar">
      <input type="search" placeholder="Search company or position" />
      <select>
        <option>All statuses</option>
        <option>Applied</option>
        <option>Interview</option>
        <option>Offer</option>
        <option>Accepted</option>
        <option>Rejected</option>
      </select>
    </div>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Company</th>
            <th>Position</th>
            <th>Applied</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="application in applications" :key="application.id">
            <td>{{ application.company }}</td>
            <td>{{ application.position }}</td>
            <td>{{ application.appliedAt }}</td>
            <td><StatusBadge :status="application.status" /></td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="pagination">
      <button class="btn" type="button" disabled>Previous</button>
      <span>Page 1 of 1</span>
      <button class="btn" type="button" disabled>Next</button>
    </div>
  </main>
</template>
