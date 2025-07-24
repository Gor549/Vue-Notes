<template>
  <div class="card">
   <h2>{{props.title}}</h2>
   <p class="text">{{props.content}} </p>
   <p class="date"> {{props.date}}</p>
    </div>
 
</template>


<script setup >
import {defineProps} from 'vue';
 let props=defineProps(['title' , 'content' , 'date'])
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
 .text {
display: -webkit-box;
-webkit-box-orient: vertical;
-webkit-line-clamp: 3;
overflow: hidden;
}
.date{
 
  margin-top: 30px;
 text-align: right;
  color: antiquewhite;
}

</style>