<script setup>
import {ref} from 'vue';
import AddButton from './components/AddButton.vue';
import Card from './components/Card.vue';
 
</script>

<template>
   <div class="container">
  <h1 class="title">  Заметки

    </h1>
    <AddButton/>
    <div class="pix">
    <card/> 
       <card/> 
          <card/> 
             <card/> 
             </div>
             </div>
  

</template>

<style scoped>
.title{
  color: rgb(217, 160, 102);
  justify-content: center;
  text-align: center;
  font-size: 60px;
  font-weight: 900;
}
.container {
  width: 100%;
  min-height: 100vh;
  background: linear-gradient(128deg, rgba(135, 246, 180, 0.84) 12.75%, rgba(50, 180, 187, 0.67) 83.4%);
  background-image: url("https://symposium.su/wp-content/uploads/2020/07/zametki-vorsatz-600x447.jpg");

}
.pix{
  display: flex;
  gap: 50px;
  justify-content: center;
 
}



</style>
