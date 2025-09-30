<template>
<div class="home">
<section class="hero">
<h1>Лучшие ноутбуки — лучшие цены</h1>
<p>Подбери ноутбук под свои задачи: работа, учёба, игры.</p>
<router-link class="cta" to="/products">Перейти к товарам</router-link>
</section>
<section class="featured">
<h2>Популярные модели</h2>
<ProductList />
</section>
</div>
</template>


<script>
import ProductList from '../components/ProductList.vue'


export default {
name: 'Home',
components: { ProductList }
}
</script>