<template>
    <div class="wraper">
    <div class="form">
        <button class="close" @click="$emit ('onClose')" >
        <i class="fa-solid fa-circle-xmark"></i>
     
        </button>
     <p class="title"> TITLE </p>
     <input/>
     <textarea name="" id=""></textarea>
     <button class="save"> Save </button>

    </div>
    </div>
</template>


<script  setup>

</script>


<style scoped>
 .wraper{
    width: 100%;
    height: 100%;
    position: fixed;
    background-color: rgba(0,0,0,0.4);
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;

 }
 .form{
    width: 580px;
    height: 600px;
   background: linear-gradient(114.43deg, rgba(255, 255, 255, 0.6) 4%, rgba(255, 255, 255, 0.1) 100%);
   border-radius: 20%;
   border: 1px solid #fff;
   padding: 25px;
   position: relative;
 }
 .title{
    font-size: 25px;
    font-weight: 500;
    text-align: center;
    color: rgb(90, 100, 100);

 }
 input {
    width: 100%;
    height: 40px;
    margin-top: 10px;
    border: none;
    border-radius: 40px;
    margin: 10px auto;
    display: block;
 }
 textarea{
    width: 100%;
    height: 280px;
    margin-top: 30px;
    border: none;
    border-radius: 40px;
    resize: none;
    
 }

 .save{
    width: 100%;
    height: 40px;
    border-radius: 4px;
    border: none;
    margin-top: 50px;
    background: linear-gradient(90deg, #B4FBF3 0%, #23926F 100%);

;
    color: #fff;
    font-size: 25px;
    cursor: pointer;
    border-radius: 40px
;
 }

 .close{
    background: none;
    border: none;
    color: #111010;
    font-size: 35px;
    cursor: pointer;
    top: 20px;
    right: 45px;
    position: absolute;

 }
</style>