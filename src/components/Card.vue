<template>
  <h1> HELLO EWERYBODY
    </h1>
    <h2>{{props.number}}</h2>
</template>


<script setup >
import {defineProps} from 'vue';
 let props=defineProps(['number'])
</script>

<style>


</style>