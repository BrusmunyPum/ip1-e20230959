<template>
  <main class="card auth-card">
    <h1>Internship Tracker</h1>
    <form @submit.prevent>
      <div class="field">
        <label for="email">Email</label>
        <input id="email" type="email" placeholder="you@example.com" />
      </div>
      <div class="field">
        <label for="password">Password</label>
        <input id="password" type="password" />
        <span class="error">Invalid email or password</span>
      </div>
      <button class="btn btn-primary" type="submit">Log in</button>
    </form>
    <p>No account? <a href="#">Register</a></p>
  </main>
</template>
