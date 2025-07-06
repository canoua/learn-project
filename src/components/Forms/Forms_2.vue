<template>
  <div style="margin-bottom: 30px;">
    <h2>Работа с checkbox в Vue</h2>
    <input type="checkbox" v-model="checked">
    <p v-if="checked">checked</p>
  </div>

  <h2>Массив значений checkbox в Vue</h2>
  <input type="checkbox" v-model="arr" value="v1">      
  <input type="checkbox" v-model="arr" value="v2">
  <input type="checkbox" v-model="arr" value="v3">
  <ul v-for="item in arr">
    <li>{{ item }}</li>
  </ul>

  <h2>Работа с radio в Vue</h2>
  
  <input name="radio" type="radio" v-model="choice" value="v1">
  <input name="radio" type="radio" v-model="choice" value="v2">
  <input name="radio" type="radio" v-model="choice" value="v3">
  <p>{{ choice }}</p>

</template>

<script>
  export default {
    data() {
      return {
        checked: true,
        arr: [],
        choice: ''
      }
    }
  }
</script>