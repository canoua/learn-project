<template>
  <h2>Условия</h2>
  <p v-if="visible">visible</p>
  <p v-if="!visible">!visible</p>
  <div>
    <button @click="hideP" v-if="visibleP">hideP</button> 
    <button @click="hidePVisible" v-if="!visibleP">!hideP</button> 
	  <p v-if="visibleP">text</p> 
  </div>
  <div>
    <h3>Директива v-else в Vue</h3>
    <p v-if="isAdmin">+++</p>
	  <p v-else>---</p>
  </div>
  <div>
    <h3>Сложные условия</h3>
    <p v-if="day===1">пн</p>
    <p v-if="day===2">вт</p>
    <p v-if="day===3">ср</p>
    <p v-if="day===4">чт</p>
    <p v-if="day===5">пт</p>
    <p v-if="day===6">сб</p>
    <p v-if="day===7">вс</p>
  </div>
  <div>
    <h3>Директива v-else-if в Vue</h3>
    <p v-if="age < 18">подросток</p>
    <p v-else-if="age >= 19 || age <= 25">молодой человек</p>
    <p v-else-if="age > 26">мужчина</p>
    <p v-else>error</p>
  </div>
  <div>
    <h3>Условные группы в Vue</h3>
    <template v-if="conditionTemp">
      <p>1</p>
      <p>2</p>
      <p>3</p>
      
    </template>
    <button @click="hideConditionTemp">hide</button>
  </div>
</template>

<script>
  export default {
    data() {
	    return {
		    visible: false,
        visibleP: true, 
        isAdmin: false,
        day: 5,
        age: 1,
        conditionTemp: true
	    }
    },
    methods: {
      hideP: function() {
        this.visibleP = false;
      },
      hidePVisible: function() {
        this.visibleP = true;
      },
      hideConditionTemp: function() {
        this.conditionTemp = false;
      }
    }
  }
</script>