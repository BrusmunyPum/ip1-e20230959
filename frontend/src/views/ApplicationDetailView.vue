<script setup lang="ts">
import AppHeader from '../components/AppHeader.vue'
import StatusBadge from '../components/StatusBadge.vue'
</script>

<template>
  <AppHeader role="STUDENT" />
  <main class="page">
    <a href="#">&lt; Back to list</a>

    <section class="card detail">
      <div class="toolbar">
        <h1>ABA Bank · Backend intern</h1>
        <StatusBadge status="OFFER" />
      </div>
      <p>Applied on 2026-10-18</p>
      <p class="hint">Approved by Mr. Advisor on 2026-10-25</p>
      <p><strong>Notes:</strong> Second round was a live coding test.</p>
      <p>
        <strong>CV:</strong> cv-brusmuny.pdf
        <button class="btn" type="button">Download</button>
      </p>

      <!-- Student buttons; an advisor sees "Approve offer" instead (see the guard table in SPEC.md) -->
      <div class="actions">
        <button class="btn btn-primary" type="button">Accept offer</button>
        <button class="btn btn-danger" type="button">Reject</button>
      </div>
    </section>

    <section>
      <h2>Comments</h2>
      <ul class="comments">
        <li class="card">
          <p class="hint">Mr. Advisor · 2026-10-20</p>
          <p>Good offer, check the contract dates.</p>
        </li>
        <li class="card">
          <p class="hint">PUM Brusmuny · 2026-10-21</p>
          <p>Thank you, I will.</p>
        </li>
      </ul>
      <form class="toolbar" @submit.prevent>
        <input type="text" placeholder="Write a comment" />
        <button class="btn btn-primary" type="submit">Send</button>
      </form>
    </section>
  </main>
</template>

<style scoped>
.detail {
  margin-top: 1rem;
}

.detail p {
  margin: 0.5rem 0;
}

.comments {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.comments li {
  padding: 0.75rem 1rem;
}

.comments p {
  margin: 0;
}
</style>
