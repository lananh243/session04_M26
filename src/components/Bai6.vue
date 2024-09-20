<template>
  <div>
    <input type="number" v-model="inputValue" />
    <button @click="handleAdd">Add to cart</button>
    <h4>Tổng tiền hàng trong giỏ hàng: {{ totalCart }}</h4>
  </div>
</template>

<script setup>
import { ref, computed, watch } from "vue";

const inputValue = ref(0);
const cartTotal = ref(0);

const totalCart = computed(() => cartTotal.value);

const handleAdd = () => {
  cartTotal.value += inputValue.value;
  inputValue.value = 0; 
};

</script>

<style>
</style>