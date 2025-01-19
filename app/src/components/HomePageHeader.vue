<script setup>

import { RouterLink } from 'vue-router';

defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="greetings">
    <RouterLink to="/">
      <img alt="Binoculars from SVGRepo" class="ui-logo" id="uiLogo" src="@/assets/binoculars-svgrepo-com.svg" width="125" height="125" />
    </RouterLink>
    <h1 class="green">{{ msg }}</h1>
    <span>
      A project successfully created with
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </span>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: center;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings {
  flex: auto;
  align-items: center;
  text-align: center;
}

.greetings h1,
.greetings span {
  text-align: center;
}

@media (min-width: 512px) {
  .greetings h1,
  .greetings span {
    text-align: center;
  }
}
</style>
