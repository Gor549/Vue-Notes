<template>
  <button class="plus"><i class="fa-solid fa-plus"></i></button>
</template>


<script setup>

</script>

<style scoped>
.plus{
    background-color: rgb(112, 112, 185);
    position: fixed;
    right: 20px;
    bottom: 20px;
    width: 70px;
    height: 70px;
    border-radius: 50%;
    border: 4px solid;
    font-size: 30px;
    cursor: pointer;
    transition: 300ms;

}
.plus:hover{
   background-color: rgb(112, 112, 185);;
   transform: scale(1.2);
}

</style>