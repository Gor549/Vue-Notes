<template>
  <div class="card">
    <button class="close" @click.stop="$emit('delate')"> <i class="fa-solid fa-circle-xmark"></i>
     </button>
   <h2>{{props.title}}</h2>
   <p class="text">{{props.content}} </p>
   <p class="date"> {{props.date}}</p>
    </div>
 
</template>


<script setup >
import {defineProps} from 'vue';
 let props=defineProps(['title' , 'content' , 'date'])
</script>

<style scoped>
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
  position: relative;

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
 .close{
    background: none;
    border: none;
    color: #111010;
    font-size: 25px;
    cursor: pointer;
    top: 20px;
    right: 70px;
    position: absolute;
    opacity: 0;
    transition: 200ms;

 }
 .card:hover .close{
  opacity: 1;

 }

</style>