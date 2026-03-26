<template>
  <div>
    <h1 :class="className" :style="styleData">Caculator: 19 - Do Minh Khoi</h1>
    <h3>Count {{ count }}</h3>
    <button @click="increment">+</button>
    <button @click="decrement">−</button>
    <button @click="reset">Reset</button>
    <button @click="changeClass">Change Class</button>
    <h2 v-html="count"></h2>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => {
  count.value++
  styleData.value = 'font-size: '+count.value+'rem;'
}
const decrement = () => {
  count.value--
  styleData.value = 'font-size: '+count.value+'rem;'
  if (count.value < 0) {
    count.value = 0
  }
}
const reset = () => {
  count.value = 0
  styleData.value = 'font-size: 5rem;'
}
const content = "Xin chao cac ban"
const className = ref("text-red")
const styleData = ref('font-size: 5rem;')
const changeClass = () => {
  if (className.value === "text-red") {
    className.value = "text-blue"
  } else {
    className.value = "text-red"
  }
}
</script>

<style scoped>
.text-red {
  color: red;
}
.text-blue {
  color: blue;
}
</style>
