<template>
    <div class="product-list">
        <template v-if="products.length">
            <div v-for="product in products" :key="product.name">
                <product-list-element
                    :product-id="product.id"
                    :product-name="product.name"
                    :product-price="product.price">
                </product-list-element>
            </div>
        </template>
        <template>
            <p>No products to show ... </p>
        </template>
    </div>
</template>

<script>

import ProductListElement from "@/components/ProductListElement";

export default {
    name: "ProductList",
    components: {
        ProductListElement
    },
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