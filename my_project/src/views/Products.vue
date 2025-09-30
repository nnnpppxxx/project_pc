<template>
<div>
<h2>Каталог ноутбуков</h2>
<ProductList />
</div>
</template>


<script>
import ProductList from '../components/ProductList.vue'
export default { name: 'Products', components: { ProductList } }
</script>