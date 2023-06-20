<template>
    <div class="container">
        <img :src=data.thumbnail>
        <div class="detail">
            <h2>ชื่อสินค้า : {{ data.title }}</h2>
            <h2>ราคา : {{ data.price }}</h2>
            <p>{{ data.description }}</p>
        </div>
    </div>
</template>

<script setup>
const { id } = useRoute().params
const { data: data } = await useFetch("https://dummyjson.com/products/" + id)
console.log(data);
</script>

<style scoped>
.container {
    display: flex;
    justify-content: center;
}
.detail {
    padding-left: 10px;
}
</style>