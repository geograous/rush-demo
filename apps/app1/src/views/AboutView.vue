<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="inc">The button above has been clicked {{ count }} times.</button>
  </div>
</template>

<script lant="ts">
// yarn 只能够使用第三方包，不支持 workspace
// import {inc} from 'inc'
export default {
  data() {
	  return {
    	count: 0
  	}
	},
  methods: {
    inc() {
      this.count = this.count+1
    }
  }
}
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
