<template>
<article class="product-card">
<img :src="product.img" alt="" class="thumb" />
<h3>{{ product.title }}</h3>
<p class="specs">{{ product.cpu }} · {{ product.ram }}</p>
<div class="row">
<div class="price">€{{ product.price }}</div>
<div>
<button @click="viewDetails">Details</button>
<button @click="add">Add to cart</button>
</div>
</div>
</article>
</template>


<script>
export default {
name: 'ProductCard',
props: { product: { type: Object, required: true } },
methods: {
viewDetails() {
this.$router.push({ path: `/product/${this.product.id}` })
},
add() {
this.$emit('add', this.product)
}
}
}
</script>