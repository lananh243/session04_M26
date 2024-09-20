<template>
  <div>
    <input type="text" v-model="inputValue" placeholder="Nhập giá trị ở đây" />
  </div>
</template>

<script setup>
import { ref, watch } from "vue";

const inputValue = ref("");

watch(inputValue, (newValue, oldValue) => {
  console.log(`Giá trị thay đổi từ "${oldValue}" thành "${newValue}"`);
});
</script>

<style>
</style>