<script setup>
import { ref } from 'vue'
import Slide4l4 from './components/slide4l4.vue'
import Bai3 from './components/Bai3.vue'
import Bai4 from './components/Bai4.vue'
import Hello from './components/Hello.vue'
import Directives from './components/directives.vue'
import Slide5 from './components/slide5.vue'
import Bai1 from './components/Lab5-PS46986/bai1.vue'
import Bai2 from './components/Lab5-PS46986/bai2.vue'

const current = ref(Slide4l4)
</script>

<template>
  <div>
    <button @click="current = Slide4l4">Bai 1-Lab4</button>
    <button @click="current = Bai3">Bai 3-lab4</button>
    <button @click="current = Bai4">Bai 4-lab4</button>
    <button @click="current = Hello">Hello-lab4</button> 
    <button @click="current = Directives">Directives</button>
    <button @click="current = Slide5">Slide 5</button>
    <button @click="current = Bai1">Bai 1 - Lab5</button>
    <button @click="current = Bai2">Bai 2 - Lab5</button>
    <component :is="current" />
  </div>
</template>
