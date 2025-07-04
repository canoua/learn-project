<template>
  <h2>Перебор группы тегов в Vue</h2>
  <div v-for="item in items">
    <p>{{ item }}</p>
    <p class="divider"></p>
  </div>
  <ul>
    <template v-for="item in items">
      <li>{{ item }}</li>
      <li class="divider"></li>
    </template>
  </ul>
  <h3>Массив объектов в Vue</h3>
  <ul>
    <template v-for="item in hrefs">
      <li>
        <a :href="item.href">{{ item.text }}</a>
      </li>
    </template>
  </ul>
  <table>
    <tbody>
      <tr v-for="product in products">
        <td>{{ product.name }}</td>
        <td>{{ product.price }}</td>
        <td>{{ product.quantity }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
  export default {
    data() {
      return {
        items: [1, 2, 3],
        hrefs: [
          {href: '1.html', text: 'text1'},
          {href: '2.html', text: 'text2'},
          {href: '3.html', text: 'text3'},
        ],
        products: [
          {
            name: 'product1',
            price: 100,
            quantity: 5
          },
          {
            name: 'product2',
            price: 200,
            quantity: 4
          },
          {
            name: 'product3',
            price: 300,
            quantity: 3
          },
        ]
      }
    }
  }
</script>