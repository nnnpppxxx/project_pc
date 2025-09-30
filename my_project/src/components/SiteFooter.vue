<template>
<footer class="footer">
<div>© {{ year }} LaptopShop — crafted with ♥</div>
</footer>
</template>


<script>
export default {
name: 'SiteFooter',
data() {
return { year: new Date().getFullYear() }
}
}
</script>