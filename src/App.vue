<template>
  <Base/>
  <Conditions/>
  <Cycles/>
  <Styles/>
  <Forms/>
  <Components/>
</template>

<style>
  @import url('./assets/base.css');
</style>

<script>
  import Base from './components/Base.vue';
  import Conditions from './components/Conditions.vue';
  import Cycles from './components/Cycles/Cycles.vue';
  import Styles from './components/Styles.vue';
  import Forms from './components/Forms/Forms.vue';
  import Components from './components/Components.vue';
  export default {
    components: {
      Base,
      Conditions,
      Cycles, 
      Styles,
      Forms,
      Components
    }
  }
</script>


