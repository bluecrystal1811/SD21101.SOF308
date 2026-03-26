<script setup>
import { ref } from 'vue'
import Slide4l4 from './components/slide4l4.vue'
import Bai3 from './components/Bai3.vue'
import Bai4 from './components/Bai4.vue'
import Hello from './components/Hello.vue'

const current = ref(Slide4l4)
</script>

<template>
  <div>
    <button @click="current = Slide4l4">Bai 1</button>
    <button @click="current = Bai3">Bai 3</button>
    <button @click="current = Bai4">Bai 4</button>
    <button @click="current = Hello">Hello</button>

    <component :is="current" />
  </div>
</template>
