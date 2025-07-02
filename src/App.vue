<template>
  <img v-bind:src="attr"> 
  <button v-on:click="show">{{ btnText }}</button>
  <button @click="showCape">showCape</button>
  <br>
  <p>{{ changeText }}</p>
  <button @click="change">change</button>
  <p>{{ price }}</p>
  <button @click="changeCost">changeCost</button>
  <a @click.once="blockClick">modified link</a>
</template>

<script>
  export default {
    data() {
      return {
        textCape: 'cape',
        btnText: 'посмотреть время',
        attr: 'img.png',
        dateNow: new Date(),
        changeText: 'changeText',
        cost: 400,
        amount: 5
      }
    },
    methods: {
      show: function() {
        alert(this.dateNow);
      },
      showCape: function() {
        alert(this.cape(this.textCape));
      },
      cape: function(str) {
	      return str[0].toUpperCase() + str.slice(1);
      },
      change: function() {
        this.changeText = 'textDoneChange'
      },
      changeCost: function() {
        this.cost = 300;
      },
      blockClick: function() {
        alert('block');
      }
    },
    computed: {
      price: function() {
        return this.amount * this.cost;
      }
    }
  }
</script>


