<template>
  <h2>Реактивность массивов в Vue</h2>
  <ul>
    <li v-for="item in arr">
      {{ item }}
    </li>
  </ul>
  <button @click="addArr">push</button>
  <button @click="deleteFirstArr">deleteFirst</button>
  <button @click="deleteLastArr">deleteLast</button>
</template>

<script>
  export default {
    data() {
      return {
        arr: ['a', 'b', 'c'],
      }
    },
    methods:{
      addArr() {
        this.arr.push('d')
      },
      deleteFirstArr() {
        this.arr.shift()
      },
      deleteLastArr() {
        this.arr.pop()
      }
      
    }
  }
</script>