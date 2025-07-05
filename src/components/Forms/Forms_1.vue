<template>
  <h2>Двусторонняя привязка данных к инпутам в Vue</h2>
  <input v-model="message">
	<p>{{ message.toUpperCase() }}</p>
  <input v-model="number">
  <p>{{ number * number }}</p>
  <h3>Получение данных формы по событию в Vue</h3>
  <p>{{ result }}</p>
  <input type="text" v-model="number_1">
  <button @click="calc">результат</button>
  <div>
    <h3>Работа с textarea в Vue</h3>
    <textarea v-model="text"></textarea>
    <p>{{ text }}</p>
  </div>
</template>

<script>
  export default {
    data() {
      return{
        message: 'hello',
        number: 5,
        number_1: 3,
        result: 0,
        text: 'aaa'
      }
    },
    methods: {
      calc: function() {
        return this.result = this.number_1*2;
      }
    }
  }
</script>