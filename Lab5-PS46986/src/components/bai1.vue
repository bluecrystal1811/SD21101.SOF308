<template>
    <div class p-5>
        <p>{{ message }}</p>
        <button class = "btn btn-dark" @click="updateMessage">Thay doi thong diep</button>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    const message = ref('Thong diep ban dau')
    const updateMessage = () => {
        message.value = 'Thong diep da duoc thay doi!'
    }
</script>

<style lang="scss" scoped>

</style>