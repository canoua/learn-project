<template>
  <h2>Цикл в диапазоне в Vue</h2>
  <p v-for="num in 30">
    {{ num }}
  </p>
  <h3>Условия в циклах в Vue</h3>
  <ul>
    <template v-for="item in items">
      <li v-if="item > 0">
        {{ item }}
      </li>
    </template>
  </ul>
  <h3>Атрибут key в Vue</h3>
  <ul>
    <template v-for="product in products" :key="product.id">
      <li>{{ product.name }}</li>
    </template>
  </ul>
</template>

<script>
  export default {
    data() {
      return {
        items: [1, -2, 3, -4, 5],
        products: [
          {
            id: 1,
            name: 'product1',
          },
          {
            id: 2,
            name: 'product2',
          },
          {
            id: 3,
            name: 'product3',
          },
        ]
      }
    }
  }
</script>