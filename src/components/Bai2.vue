<template>
  <div>
    <h4>Company : {{content.company}}</h4>
    <h4>Age : {{content.age}}</h4>
    <button @click="handleChange">Change data</button>
  </div>
</template>

<script setup>
import {reactive} from "vue"
const content = reactive ({
    company : "Rikkei Academy",
    age : 2,
})

const handleChange = () => {
    content.company = "Rikkei Education";
    content.age --;
}
</script>

<style>

</style>