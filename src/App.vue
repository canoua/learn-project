<script setup>
  import { ref, computed } from 'vue'
  import Home from './views/Base.vue';
  import Styles from './views/Styles.vue';
  import Conditions from './views/Conditions.vue';
  import Cycles from './views/Cycles.vue';

  const routes = {
    '/': Home,
    '/cycles': Cycles,
    '/styles': Styles,
    '/conditions': Conditions
  }

  const currentPath = ref(window.location.hash)

  window.addEventListener('hashchange', () => {
    currentPath.value = window.location.hash
  })

  const currentView = computed(() => {
    return routes[currentPath.value.slice(1) || '/'] || NotFound
  })
  
</script>

<template>
  <a href="#/">Base</a> |
  <a href="#/cycles">Cycles</a> |
  <a href="#/styles">Styles</a>|
  <a href="#/conditions">Conditions</a>
  <component :is="currentView" />
</template>

