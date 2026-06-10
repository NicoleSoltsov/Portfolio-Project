<script setup>
import { ref } from 'vue'
import { RouterView, RouterLink } from 'vue-router'
import IntroAnimation from './components/IntroAnimation.vue'

const showIntro = ref(true)
</script>

<template>
  <IntroAnimation
    v-if="showIntro"
    @finished="showIntro = false"
  />

  <div v-else>
    <nav class="navbar">
      <RouterLink to="/" class="logo">
        Nicole Soltsov
      </RouterLink>

      <div class="nav-links">
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/experience">Experience</RouterLink>
        <RouterLink to="/projects">Projects</RouterLink>
      </div>
    </nav>

    <RouterView />
  </div>
</template>

<style>
:root {
  --cream: #faf7f2;
  --blush: #f4d6dc;
  --powder-blue: #dbe8f5;
  --sage: #dfe9de;
  --butter: #f8e8b8;
  --ucla-blue: #2774ae;
  --charcoal: #2d2d2d;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body,
#app {
  min-height: 100vh;
}

body {
  background: var(--cream);
  color: var(--charcoal);
  font-family: "Avenir Next", "SF Pro Display", Helvetica, Arial, sans-serif;
}

.navbar {
  width: 100%;
  padding: 24px 8%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  text-decoration: none;
  color: var(--charcoal);
  font-size: 1.4rem;
  font-weight: 700;
}

.nav-links {
  display: flex;
  gap: 18px;
}

.nav-links a {
  text-decoration: none;
  color: var(--charcoal);
  background: white;
  padding: 10px 20px;
  border-radius: 999px;
  transition: all 0.25s ease;
}

.nav-links a:hover {
  background: var(--blush);
  transform: translateY(-2px);
}

.router-link-active {
  background: var(--powder-blue) !important;
  color: var(--ucla-blue) !important;
}

@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    gap: 16px;
  }

  .nav-links {
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>