<template>
    <!-- Hiển thị lời chào -->
    <h1>{{ greeting }}</h1>
    <button @click="changeGreeting">Đổi lời chào</button>
    <button @click="changeClass">Change Class</button>
        <h2 v-bind:title="buttonTitle" :class="className" v-html="greeting"></h2>
</template>
<script setup>
import { ref } from 'vue';
const buttonTitle = ref('xin chào')
const greeting = ref('Lời chào ban đầu')
const className = ref("text-red")
const changeGreeting = () => {
    buttonTitle.value = 'Hi'
    greeting.value = 'Lời chào đã được thay đổi'
}
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
