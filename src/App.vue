<script setup>
  import { ref, computed } from 'vue'
  import Home from './views/Base.vue';
  import Styles from './views/Styles.vue';
  import Conditions from './views/Conditions.vue';
  import Cycles from './views/Cycles.vue';
  import Forms from './views/Forms.vue';
  import Components from './views/Components.vue';

  const routes = {
    '/': Home,
    '/cycles': Cycles,
    '/styles': Styles,
    '/conditions': Conditions,
    '/forms': Forms,
    '/components': Components
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
  <div style="text-align: center;">
    <a href="#/">Основы</a> |
    <a href="#/cycles">Циклы</a> |
    <a href="#/styles">Стили</a>|
    <a href="#/conditions">Условия</a> |
    <a href="#/forms">Формы</a> |
    <a href="#/components">Компоненты</a>
    <component :is="currentView" />
  </div>
  
</template>

