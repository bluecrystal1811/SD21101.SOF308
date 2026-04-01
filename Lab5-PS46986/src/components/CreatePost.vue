<template>
  <div class="mb-4">
    <h2 class="h3 mb-3 text-center">Tạo bài viết mới</h2>

    <div class="mb-3">
      <input v-model="title" class="form-control" placeholder="Tiêu đề bài viết" />
    </div>

    <div class="mb-3">
      <input v-model="author" class="form-control" placeholder="Tên tác giả" />
    </div>

    <div class="mb-3">
      <textarea v-model="content" class="form-control" rows="4" placeholder="Nội dung bài viết"></textarea>
    </div>

    <div class="text-center">
      <button class="btn btn-primary px-4" @click="submitPost">Đăng bài</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const emit = defineEmits(['add-post'])

const title = ref('')
const content = ref('')
const author = ref('')

function submitPost() {
  if (title.value && content.value && author.value) {
    const newPost = {
      title: title.value,
      content: content.value,
      author: author.value,
    }

    emit('add-post', newPost)

    title.value = ''
    content.value = ''
    author.value = ''
  }
}
</script>

<style scoped></style>
