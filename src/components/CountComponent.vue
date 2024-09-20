<template>
  <div>
    <h2>Count : {{ count }}</h2>
    <button @click="handleCount">Count</button><br />
    <h2>Random : {{ randomNumber }}</h2>
    <button @click="handleRandom">Random</button><br />
    <h2>{{ numbers }}</h2>
    <button @click="handlePush">Push number</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const count = ref(0);
const randomNumber = ref(1);

const numbers = ref([]);
// Khi dùng ref
// Để cập nhật lại giá trị thì bắt bc phải truy cập vào value
// Khi sử dụng thì ko cần dùng value

const handleCount = () => {
  // Cập nhật lại giá trị của count
  count.value++;
};

const handleRandom = () => {
  // Tạo số ngẫu nhiên từ 1 -> 10
  const random = Math.floor(Math.random() * 10);
  // Gán lại giá trị cho biến randomNuber
  randomNumber.value = random;
};

const handlePush = () => {
  const random = Math.ceil(Math.random() * 10); 
    // Push số random vào mảng và cập nhật lại giá trị cho mảng numbers
    // Cách 1
    // numbers.value.push(random); 
    // Cách 2 
    numbers.value = [...numbers.value, random]
};
</script>

<style></style>
