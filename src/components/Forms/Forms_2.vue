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

  <div>
    <h2>Работа с select в Vue</h2>
    <select v-model="selected">
      <option>val1</option>
      <option>val2</option>
      <option>val3</option>
    </select>
    <p>{{ selected }}</p>
  </div>

  <div>
    <h2>Формирование select в цикле в Vue</h2>
    <select v-model="selected">
      <option v-for="option in options">{{ option }}</option>
    </select>
    <p>{{ selected }}</p>
  </div>

  <div>
    <h2>Блокировка элементов в Vue</h2>
    <button v-bind:disabled="isDisabled">btn</button>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        checked: true,
        arr: [],
        choice: '',
        selected: 'val1',
        options: ['1','2','3'],
        isDisabled: true
      }
    }
  }
</script>