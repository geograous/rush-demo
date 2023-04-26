<template>
  <div class="about">
    <div>
      <h1>This is an about page</h1>
      <button @click="inc">The button above has been clicked {{ count }} times.</button>
    </div>
  </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
// yarn 只能够使用第三方包，不支持 workspace
// import {inc} from 'inc'

const count = ref(0)

const inc = () => {
  count.value = count.value+1
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
