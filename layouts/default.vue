<template>
    <div>
        <header>
            <nav>
                <h1 class="logo">Navbar</h1>
                <NuxtLink to="/">หน้าแรก</NuxtLink>
                <NuxtLink to="/products">สินค้า</NuxtLink>
                <NuxtLink to="/about">เกี่ยวกับเรา</NuxtLink>
            </nav>
        </header>
    </div>
    <div>
        <slot/>
    </div>
</template>

<script setup>

</script>

<style scoped>
nav {
    display: flex;
    justify-content: center;
    align-items: center;
    background: #333;
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 10px;
    padding: 10px;
    font-size: 20px;
}

nav a:hover {
    color: orange;
}

.logo {
    margin-right: auto;
    padding: 10px;
    color: white;
}
</style>