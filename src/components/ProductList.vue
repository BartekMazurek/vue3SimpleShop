<template>

    <div class="product-list">
        <template v-if="products.length">
            <div v-for="product in products" :key="product.name">
                <product-list-element
                    :product-id="product.id"
                    :product-name="product.name"
                    :product-price="product.price"
                    @showProductDetailsComponent="getProductDetails">
                </product-list-element>
            </div>
        </template>
        <template>
            <p>No products to show ... </p>
        </template>
    </div>

    <component
        v-if="showProductDetailsComponent"
        :is="productDetailsComponentName"
        :product-id-to-show-details="productIdToShowDetails">
    </component>

</template>

<script>

import ProductListElement from "@/components/ProductListElement";
import ProductListElementDetails from "@/components/ProductListElementDetails";

export default {
    name: "ProductList",
    components: {
        ProductListElement
    },
    props: {
        products: Array
    },
    data: () => ({
        productIdToShowDetails: 0,
        showProductDetailsComponent: false,
        productDetailsComponentName: ProductListElementDetails
    }),
    methods: {
        getProductDetails: function (event) {
            this.showProductDetailsComponent = true;
            this.productIdToShowDetails = event;
        }
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