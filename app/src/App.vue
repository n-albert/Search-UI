<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <RouterView />
</template>

<style scoped>

.container {
  width: 100%;
  height: 500px;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

header span {
  display: inline-block;
  text-align: center;
}

.ui-logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  margin-top: 2rem;
  text-align: center;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 512px) {
  header {
    display: flex;
    flex-direction: column;
    place-items: center;
  }

  .ui-logo {
    margin: 0 0 0 0;
  }


  nav {
    text-align: center;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
