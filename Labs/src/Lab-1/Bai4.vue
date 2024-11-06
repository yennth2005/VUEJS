<template>
    <div class="container mt-5">
      <h1 class="text-center">Danh sách sản phẩm bài 4 lab 1</h1>
      <div class="row">
        <template v-for="product in products" :key="product.id"> <div class="col-sm-4">
            <div class="card">
              <img :src="product.image" alt="image" class="card-img-top" />
              <div class="card-body">
                <h3 class="card-title">{{ product.name }}</h3>
                <p class="card-text">{{ product.description }}</p>
                <p class="card-text">Giá: {{ product.price }} VND</p>
                <button class="btn btn-danger">Mua ngay</button>
              </div>
            </div>
          </div>
        </template>
      </div>
    </div>
  </template>
  
  <script setup>
  
  const products = [
    {
      id: 1,
      name: "Nike Air M1",
      description: "Giày thể thao Nike Air M1",
      price: 500000,
      image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGeJ3l5DlcUnNjqh3YKISyjT0CckkIT5PmLCOQdyT8NzSaRoHtO_7jYkL7-2keMOm2UBI&usqp=CAU"
    },
    {
      id: 2, 
      name: "Nike Air M1",
      description: "Giày thể thao Nike Air M1",
      price: 300000,
      image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSDPmYbz9IX9bzyOc4CcDYduYMANxLbp0Czg&s"
    },
    {
      id: 3, 
      name: "Nike Air M1",
      description: "Giày thể thao Nike Air M1",
      price: 1000000,
      image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGeJ3l5DlcUnNjqh3YKISyjT0CckkIT5PmLCOQdyT8NzSaRoHtO_7jYkL7-2keMOm2UBI&usqp=CAU"
    }
  ];
  
  
  </script>