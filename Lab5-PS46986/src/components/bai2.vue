<template>
    <div>
        <input v-model = "userInput" placeholder = "Nhap du lieu vao day"/>
        <p>Gia tri vua nhap: {{ userInput }}</p>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    const userInput = ref('FPL');
</script>

<style lang="scss" scoped>

</style>