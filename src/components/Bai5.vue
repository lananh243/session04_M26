<template>
  <div>
    <h3>Giỏ hàng</h3>
    <ul>
        <li>Mèn mén Loại 1 - Số lượng : {{count}} <button @click="handleCount">Tăng số lượng</button></li>
        <li>Mèn mén Loại 2 - Số lượng : {{count2}} <button @click="handleCount2">Tăng số lượng</button></li>
        <li>Mèn mén Loại 2 - Số lượng : {{count3}} <button @click="handleCount3">Tăng số lượng</button></li>
    </ul>
    <h4>Tổng số lượng sản phẩm : {{totalCount}}</h4>
  </div>
</template>

<script setup>
import {ref, computed, watch} from "vue"
const count = ref(0)
const count2 = ref(0)
const count3 = ref(0)
const handleCount = () => {
    count.value++;
}
const handleCount2 = () => {
    count2.value++;
}
const handleCount3 = () => {
    count3.value++;
}
const totalCount = computed(() => {
    return count.value + count2.value + count3.value
})

watch(totalCount, (newValue, oldValue) => {
    console.log(`Giá trị ${newValue} - Giá trị ${oldValue}`);
    
})
</script>

<style>

</style>