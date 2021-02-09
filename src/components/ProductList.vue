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

    <template v-if="showProductDetailsComponent">
        <product-list-element-details
            :product-id="productId"
            :product-description="productDescription"
            @closeProductDetailsWindow="hideProductDetails">
        </product-list-element-details>
    </template>

</template>

<script>

import ProductListElement from "@/components/ProductListElement";
import ProductListElementDetails from "@/components/ProductListElementDetails";
import ProductDetails from "@/service/ProductDetails/ProductDetails";

export default {
    name: "ProductList",
    components: {
        ProductListElementDetails,
        ProductListElement
    },
    props: {
        products: Array
    },
    data: () => ({
        productId: 0,
        productDescription: '',
        showProductDetailsComponent: false,
        productDetailsComponentName: ProductListElementDetails
    }),
    methods: {
        getProductDetails: function (event) {
            this.productId = event;
            const productDetailsService = new ProductDetails();
            this.productDescription = productDetailsService.getProductDetailsById(this.productId);
            this.showProductDetailsComponent = true;
        },
        hideProductDetails: function(event) {
            this.showProductDetailsComponent = event;
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