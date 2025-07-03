<template>
  <h2>Styles</h2>
  <p>1</p>
  <p :class="str">text</p>
  <p :class="obj">text</p>
  <p :class="obj_2">text</p>
  <button @click="hide">hide</button>
  <p :class="{active: true, error: false}">
		text
	</p>
  <p :class="{valid: true, disabled: false}">text</p>
</template>

<style scoped>
  p {
    color: brown;
  }
  p.hidden {
	  display: none;
  }
</style>

<script>
  export default {
    data() {
      return {
        str: 'active valid',
        obj: {
          active: true,
          valid:  false,
        },
        obj_2: {
			    hidden: true,
		    },
        isValid: true,
		    isDisabled: true,
      }
    },
    methods: {
      hide: function() {
        this.obj_2.hidden = !this.obj_2.hidden;
      }
    }
  }
</script>