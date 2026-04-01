<template>
    <div class="col-lg-7 mx-auto py-3">
        <h1 class="text-center">Thông tin cá nhân</h1>
        <form>
            <div class="m-3">
                <label>Họ tên</label>
                <input v-model="userInfo.name" type="text" class="form-control" placeholder="Nhập họ tên">
            </div>
            <div class="m-3">
                <label>Tuổi</label>
                <input v-model="userInfo.age" type="number" class="form-control" placeholder="Nhập tuổi">
            </div>
            <div class="m-3">
                <label>Email</label>
                <input v-model="userInfo.email" type="email" class="form-control" placeholder="Nhập email">
            </div>
        </form>
        <!-- Hiển thị thông tin ngay sau khi nhập -->
        <div class="info-display mt-4 p-3 bg-dark text-white rounded">
            <h3>Thông tin đã nhập:</h3>
            <p><strong>Họ tên:</strong> {{ userInfo.name }}</p>
            <p><strong>Tuổi:</strong> {{ userInfo.age }}</p>
            <p><strong>Email:</strong> {{ userInfo.email }}</p>
        </div>
    </div>
</template>

<script setup>
    import { reactive } from 'vue';
    // Khởi tạo đối tượng thông tin người dùng sử dụng reactive để tạo reactivity
    const userInfo = reactive({
        name: '',
        age: null,
        email: ''
    });
</script>

<style lang="scss" scoped></style>