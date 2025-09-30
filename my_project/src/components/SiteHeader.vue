<template>
<header class="header">
<div class="logo">LaptopShop</div>
<nav class="nav">
<router-link to="/">Home</router-link>
<router-link to="/products">Laptops</router-link>
<router-link to="/cart">Cart ({{ cartCount }})</router-link>
</nav>
</header>
</template>


<script>
import { useProductsStore } from '../store/products'


export default {
name: 'SiteHeader',
data() {
return {
}
},
computed: {
cartCount() {
const store = useProductsStore()
return store.cartCount
}
}
}
</script>