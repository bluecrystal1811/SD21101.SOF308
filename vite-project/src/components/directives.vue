<template>
    <div>
        <button @click="show = !show">Click me show</button>
        <h1 v-if="show">{{ message }}</h1>
        <hr>
        <h2 v-show="!show" v-html="message"></h2>
    </div>
    <div>
        <input type="text" v-model="message" />
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    const message = ref('FPT Polytechnic')
    const show = ref(true)
</script>

<style lang="scss" scoped>

</style>