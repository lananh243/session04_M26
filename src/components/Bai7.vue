<template>
  <div>
    <input type="number" v-model="inputValue" placeholder="Nhập giá trị" />
    <button @click="handleAdd">Add to cart</button>
    <h4>Tổng tiền hàng trong giỏ hàng: {{ cartTotal }}</h4>
    <h4>Giá trị bình phương: {{ square }}</h4>
  </div>
</template>

<script setup>
import { ref, computed, watch } from "vue";

const inputValue = ref(0); 
const cartTotal = ref(0);   

const square = computed(() => {
  return inputValue.value ** 2;
});

const handleAdd = () => {
  cartTotal.value += inputValue.value; 
  inputValue.value = 0; 
};

watch(cartTotal, (newValue, oldValue) => {
  console.log(`Giá trị mới: ${newValue} - Giá trị cũ: ${oldValue}`);
});
</script>

<style>
</style>