<template>
<div class="search">
  <input  @keydown.enter="$emit('onSearch',text)"   v-model="text" type="search">
  <button @click="$emit('onSearch',text)"><i class="fa-solid fa-magnifying-glass"></i></button>
</div>
</template>

<script setup>
import {ref} from 'vue';
let text = ref('')
</script>

<style scoped>
.search{
    width: 350px;
    height: 40px;
    display: flex;
    border-radius: 40px;
}
input{
    flex: 1;

}
button{
    width: 40px;
    height: 40px;
    border-radius: 40px;
    background:  rgb(112, 112, 185);

}
</style>