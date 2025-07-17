<script setup>
import {ref} from 'vue';
 import Card from'./components/Card.vue'
let number = ref(7)
const increment = () =>{
  number.value++
}
</script>

<template>
  <div>
    <Card :number="number"/>
    <button @click="increment">Click me</button>
  </div>

</template>

<style scoped>
h1 {
  color: aqua;
}

h2 {
  color: brown;
}
</style>
