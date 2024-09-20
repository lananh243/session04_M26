<template>
  <div>
    <h1>Reactive</h1>
    <br>
    <p>Id : {{userInfo.id}}</p>
    <p>UserName : {{userInfo.userName}}</p>
    <button @click="handleIncreaseId">Increase Id</button>
  </div>
</template>

<script setup>
import { reactive }  from "vue";

const userInfo = reactive ({
    id:1,
    userName: "Nguyễn Văn A"
});
const handleIncreaseId = () => {
    userInfo.id++;
}
</script>

<style>

</style>