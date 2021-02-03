<template>
    <div class="product-list">

        <template v-if="products.length">
            <div v-for="product in products" :key="product.name">
                <p>Id: {{ product.id }} | Name: {{ product.name }} | Price {{ product.price }}</p>
            </div>
        </template>

        <template>
            <p>No products to show ... </p>
        </template>

    </div>
</template>

<script>

export default {
    name: "ProductList",
    props: {
        products: Array
    }
}

</script>

<style scoped>
.product-list {
    margin-top: 20px;
    border: 1px solid #ff5a00;
    min-height: 100px;
}
</style>