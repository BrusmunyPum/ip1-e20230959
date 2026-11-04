<script setup lang="ts">
import AppHeader from '../components/AppHeader.vue'
import StatusBadge from '../components/StatusBadge.vue'

// Static sample rows for Check 1; they move to a Pinia store with mock data at Check 2.
const applications = [
  { id: 3, student: 'PUM Brusmuny', company: 'ABA Bank', position: 'Backend intern', status: 'OFFER' },
  { id: 4, student: 'SOK Dara', company: 'Wing Bank', position: 'Data intern', status: 'INTERVIEW' },
] as const
</script>

<template>
  <AppHeader role="ADVISOR" />
  <main class="page">
    <h1>Students' applications</h1>

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
            <th>Student</th>
            <th>Company</th>
            <th>Position</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="application in applications" :key="application.id">
            <td>{{ application.student }}</td>
            <td>{{ application.company }}</td>
            <td>{{ application.position }}</td>
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
