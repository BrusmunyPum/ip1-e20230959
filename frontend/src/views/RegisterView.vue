<template>
  <main class="card auth-card">
    <h1>Create a student account</h1>
    <form @submit.prevent>
      <div class="field">
        <label for="fullName">Full name</label>
        <input id="fullName" type="text" />
      </div>
      <div class="field">
        <label for="email">Email</label>
        <input id="email" type="email" placeholder="you@example.com" />
        <span class="error">Email is already registered</span>
      </div>
      <div class="field">
        <label for="password">Password</label>
        <input id="password" type="password" />
        <span class="hint">At least 8 characters</span>
      </div>
      <button class="btn btn-primary" type="submit">Register</button>
    </form>
    <p>Already have an account? <a href="#">Log in</a></p>
  </main>
</template>
