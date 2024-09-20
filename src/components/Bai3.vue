<template>
  <div>
    <h3>Acreage: {{ acreage }}</h3>
    <button @click="handleIncrease">Change data</button>
  </div>
</template>

<script setup>
import { ref, computed } from "vue"; 

const width = ref(10); 
const height = ref(20);

// Tính diện tích
const acreage = computed(() => {
  return width.value * height.value;
});
const handleIncrease = () => {
  width.value += 10; 
};
</script>

<style>
</style>