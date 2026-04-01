<script setup>
import { ref } from 'vue'
import bai1 from './components/bai1.vue'
import bai2 from './components/bai2.vue'
import bai3 from './components/bai3.vue'
import CreatePost from './components/CreatePost.vue'
import PostList from './components/PostList.vue'

const current = ref('blog')
const views = {
  bai1,
  bai2,
  bai3,
}

const posts = ref([])

function addPost(post) {
  posts.value.push(post)
}
</script>

<template>
  <div id="app" class="container py-4">
    <div class="d-flex justify-content-center mb-4 flex-wrap gap-2">
      <button class="btn btn-outline-primary" @click="current = 'bai1'">Bài 1</button>
      <button class="btn btn-outline-primary" @click="current = 'bai2'">Bài 2</button>
      <button class="btn btn-outline-primary" @click="current = 'bai3'">Bài 3</button>
      <button class="btn btn-primary" @click="current = 'blog'">Blog</button>
    </div>

    <div v-if="current === 'blog'" class="card shadow-sm border-0">
      <div class="card-body p-4 p-md-5">
        <h1 class="display-5 fw-bold text-center mb-4">Ứng dụng Blog nhỏ với Vue.js</h1>
        <CreatePost @add-post="addPost" />
        <PostList :posts="posts" />
      </div>
    </div>

    <component v-else :is="views[current]" />
  </div>
</template>
