<template>
  <h2>Форма для добавления элементов массива в Vue</h2>
  <input type="text" v-model="newItem">
  <button @click="addTask">добавить дело</button>
  <ul v-for="item in items">
    <li>{{ item }}</li>
  </ul>
</template>

<script>
  export default {
    data() {
      return {
        newItem: '',
        items: ['abc', 'cde', 'fgh']
      }
    },
    methods: {
      addTask: function() {
        this.items.unshift(this.newItem);
        // alert(this.items);
      }
    }
  }
</script>