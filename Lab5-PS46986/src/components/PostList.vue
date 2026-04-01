<template>
  <div>
    <h2 class="h3 mt-4 mb-3 text-center">Danh sách bài viết</h2>

    <p v-if="posts.length === 0" class="text-center text-muted">Chưa có bài viết nào. Hãy tạo bài viết đầu tiên.</p>

    <div
      v-for="(post, index) in posts"
      :key="index"
      class="post card shadow-sm mb-3 highlighted"
      :style="{ backgroundColor: post.backgroundColor || '#ffffff', color: post.textColor || '#222222' }"
    >
      <div class="card-body text-start">
        <h3 class="h5 fw-bold mb-2">{{ post.title }}</h3>
        <h4 class="h6 mb-3">
          <span class="badge text-bg-danger">{{ post.author }}</span>
        </h4>
        <p class="mb-0">{{ post.content }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  posts: {
    type: Array,
    required: true,
  },
})
</script>

<style scoped>
.post {
  border-radius: 0.85rem;
  border: 1px solid rgba(0, 0, 0, 0.1);
}

.highlighted {
  border-left: 0.35rem solid #0d6efd;
}
</style>
