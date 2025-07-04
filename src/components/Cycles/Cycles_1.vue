<template>
  <h2>Cycles-1</h2>
  <p v-for="item in items">{{ item * item }}</p>
  <ul>
    <li v-for="item in items">{{ item }}</li>
  </ul>
  <h3>Получение ключей при переборе массивов в Vue</h3>
  <ul>
    <li v-for="(elem, key) in arr">
      {{ key }} {{ elem }}
    </li>
  </ul>
  <h3>Перебор объектов в Vue</h3>
  <ul>
    <li v-for="elem in users">
      {{ elem }}
    </li>
  </ul>
  <ul>
    <li v-for="(elem, key) in users">
      {{ key }} - {{ elem }}
    </li>
  </ul>
  <ul>
    <li v-for="(elem, key, index) in users">
      {{ key }} - {{ elem }} - {{ index }}
    </li>
  </ul>
  <ul>
    <li v-for="(elem, key, index) in users">
      {{ key }} - {{ elem }} - {{ index+1 }}
    </li>
  </ul>
</template>

<script>
  export default {
    data() {
      return{
        items: [1, 2, 3, 4, 5],
        arr: ['x', 'y', 'z'],
        users: {
          user1: '100$',
	        user2: '200$',
	        user3: '300$',
        }
      }
    }
  }
</script>