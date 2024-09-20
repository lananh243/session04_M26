<template>
  <div>
    <h1>Count : {{count}}</h1>
    <button @click="handleCount">Count</button>
  </div>
</template>

<script setup>
import {ref, watch} from "vue"
const count = ref(0);
const handleCount = () => {
    count.value++;
}
watch(count, (newValue, oldValue) => {
    // Lắng nghe sự thay đổi của count
    console.log(`old value : ${oldValue} - New value : ${newValue}`);
    
})
</script>

<style>

</style>