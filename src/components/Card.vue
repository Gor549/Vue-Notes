<template>
  <div class="card">
   <h2>My Title</h2>
   <p class="text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the </p>
   <p class="date"> 27.05.2025 21:21</p>
    </div>
 
</template>


<script setup >
import {defineProps} from 'vue';
 let props=defineProps(['number'])
</script>

<style>
 .card {
  display: flex;
  border-radius: 50%;
background: linear-gradient(114.43deg, rgba(136, 108, 108, 0.6) 4%, rgba(255, 255, 255, 0.1) 100%);
  width: 340px;
  height: 290px;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 20px;

 }
 h2{
  margin-bottom: 30px;
 }
 
</style>