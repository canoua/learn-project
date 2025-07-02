<template>
  <Base/>
  <Conditions/>
  <Cycles/>
  <Styles/>
  <Forms/>
  <Components/>
</template>

<script>
  import Base from './components/Base.vue';
  import Conditions from './components/Conditions.vue';
  import Cycles from './components/Cycles.vue';
  import Styles from './components/Styles.vue';
  import Forms from './components/Forms.vue';
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


