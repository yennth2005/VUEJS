<template>
    <div class="rows">
        <!-- interpolation: nội suy (nhúng js vào html tạo ra nội dung động) //hiển thị dữ liệu động trong giao diện
        cú pháp {{  }} 
    -->
        <!-- Hiển thị lời chào -->
        <h1>{{ greeting }}</h1>
        <!-- v-bind: là chỉ thị trong vue, dùng để ràng buộc các thuộc tính của phần tử html với các biểu thức trong dữ liệu của vue
        cú pháp: v-bind:attribute="expression" VIẾT TẮT :attribute="expression"
        //tạo ra thuộc tính động cho phần tử html
    -->
        <!-- v-on: là chỉ thị của vue để lắng nghe sự kiện của phần tử html và thực thi phương thức trong vue khi sự kiện xảy ra 
        cú pháp: v-on@click="hanleClick VIẾT TẮT @click="handleClick"" 
        //lắng nghe và xử lý sự kiện
    -->
        <!-- Tạo nút thay đổi nội dung -->
        <button class="btn btn-info" :title="buttonTitle" @click="changeGreeting">Click để thay đổi</button>
    </div>
</template>
<script setup>
import { ref } from "vue";
// ref trong vue 
// Khai báo biến reactive
// state 
const greeting = ref("Xin chào, đây là bài 3 lab 1");
const buttonTitle = ref("Nhấn để thay đổi lời chào");
// Khai báo hàm thay đổi lời chào
const changeGreeting = () => {
    greeting.value = "Hello, World!";
    buttonTitle.value = "Lời chào mới đã được cập nhật";
};
</script>