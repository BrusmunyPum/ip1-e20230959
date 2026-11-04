<script setup lang="ts">
import { ref } from 'vue'
import LoginView from './views/LoginView.vue'
import RegisterView from './views/RegisterView.vue'
import ApplicationListView from './views/ApplicationListView.vue'
import ApplicationDetailView from './views/ApplicationDetailView.vue'
import ApplicationFormView from './views/ApplicationFormView.vue'
import AdvisorListView from './views/AdvisorListView.vue'
import ProfileView from './views/ProfileView.vue'
import NotFoundView from './views/NotFoundView.vue'

// Check 1 has no router yet: this bar only lets us preview each static screen.
// Vue Router replaces it at Check 2.
const screens = [
  { name: 'Login', component: LoginView },
  { name: 'Register', component: RegisterView },
  { name: 'My applications', component: ApplicationListView },
  { name: 'Application detail', component: ApplicationDetailView },
  { name: 'Add application', component: ApplicationFormView },
  { name: "Students' applications", component: AdvisorListView },
  { name: 'Profile', component: ProfileView },
  { name: 'Not found', component: NotFoundView },
]

const current = ref(screens[0]!)
</script>

<template>
  <div class="screen-picker">
    <span>Preview:</span>
    <button
      v-for="screen in screens"
      :key="screen.name"
      type="button"
      :class="{ active: screen === current }"
      @click="current = screen"
    >
      {{ screen.name }}
    </button>
  </div>

  <component :is="current.component" />
</template>

<style scoped>
.screen-picker {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.25rem;
  padding: 0.5rem 1rem;
  background: #1f2933;
  color: #fff;
  font-size: 0.8rem;
}

.screen-picker button {
  font: inherit;
  padding: 0.2rem 0.6rem;
  border: 1px solid #52606d;
  border-radius: 4px;
  background: transparent;
  color: #fff;
  cursor: pointer;
}

.screen-picker button.active {
  background: #fff;
  color: #1f2933;
}
</style>
