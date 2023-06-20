<template>
    <div class="container">
        <div  v-for="product in data.products">
            <NuxtLink :to="`/products/${product.id}`">
                <h2 class="title">{{ product.title }}</h2>
            </NuxtLink>
            <img :src=product.thumbnail>
        </div>
    </div>
</template>

<script setup>
const { data: data } = await useFetch('https://dummyjson.com/products')
</script>

<style  scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
.container div{
    width:300px;
    height:300px;
    margin: 30px 15px; 
    background-color:#333;
}
.title {
    color:white;
    text-align: center;
    font-size: 1rem;
    text-decoration: none;
}
.title:hover {
    color: orange;
}
img{
    width: 300px;
    height: 300px;
}
</style>