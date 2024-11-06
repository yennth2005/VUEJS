<template>
    <div class="container">
        <h1>Quản lý giỏ hàng với ref()</h1>
        <button class="btn btn-outline-danger" @click="decreaseCount" :disabled="productCount === 0">-</button>
        <p>Số lượng sản phẩm: {{ productCount }}</p>
        <button class="btn btn-outline-info" @click="increaseCount">+</button>
    </div>
</template>
<script setup>
import { ref } from "vue";
const productCount = ref(0);
const increaseCount = () => {
    productCount.value++;
};
const decreaseCount = () => {
    if (productCount.value > 0) {
        productCount.value--;
    }
};
</script>