<template>
<section class="product-list">
<ProductCard
v-for="p in products"
:key="p.id"
:product="p"
@add="onAddToCart"
/>
</section>
</template>


<script>
import ProductCard from './ProductCard.vue'
import { useProductsStore } from '../store/products'


export default {
name: 'ProductList',
components: { ProductCard },
computed: {
products() {
const store = useProductsStore()
return store.products
}
},
methods: {
onAddToCart(product) {
const store = useProductsStore()
store.addToCart(product)
this.$router.push('/cart')
}
}
}
</script>