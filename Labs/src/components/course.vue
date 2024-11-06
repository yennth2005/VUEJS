<template>
    <div class="container">
        <h1>Thông tin khoá học</h1>
        <ul class="list-group list-group-numbered">
            <li class="list-group-item active">Thông tin khoá học </li>
            <li class="list-group-item">Tên khoá học: {{ courseName }}</li>
            <li class="list-group-item">Cấp độ: {{ info.level }}</li>
            <li class="list-group-item disabled">Thời gian: {{ info.time }} </li>
            <li class="list-group-item disabled">Trạng thái: <span class="badge":class="{'rounded-pill text-bg-success':info.isOpen,'rounded-pill text-bg-danger':!info.isOpen,}">{{ info.isOpen ? 'Mở' :"Đóng"}}</span>   </li>
        </ul>
        
    </div>
</template>
<script setup>
import { ref } from 'vue';

    const courseName="VueJs";
    const info={
        level: "Cao cấp",
        time: '2h',
        isOpen: false  
    }
    
</script>
<style scoped></style>