<template>
    <div class="product-list-element">
        <div class="list-element-content">
            <div class="list-element-image">
                <img :src="require(`@/assets/images/products/${ productId }.jpg`)" alt class="picture"/>
            </div>
            <div class="list-element-info">
                <div class="product-name">
                    <p @click="showProductDetails">{{ productName }}</p>
                </div>
                <div class="product-price">
                    <p>{{ productPrice }}</p>
                    <p>€</p>
                </div>
            </div>
        </div>
        <div class="bottom-line"></div>
    </div>

</template>

<script>

export default {
    name: "ProductListElement",
    props: {
        productId: Number,
        productImage: String,
        productName: String,
        productPrice: Number
    },
    methods: {
        showProductDetails: function() {
            this.$emit('showProductDetailsComponent', this.productId);
        }
    }
}

</script>

<style scoped>

.product-list-element {
    padding: 60px;
}

.product-list-element .list-element-image {
    position: relative;
    top: -45px;
    width: 30%;
    float: left;
}

.product-list-element .list-element-image img {
    height: 130px;
}

.product-list-element .list-element-info {
    width: 70%;
    margin-right: 0;
    margin-left: auto;
}

.product-list-element .list-element-info div {
    display: inline-block;
}

.product-list-element .list-element-info .product-name {
    position: relative;
    top: 15px;
    width: 60%;
}

.product-list-element .list-element-info .product-name p {
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;
}

.product-list-element .list-element-info .product-price {
    text-align: right;
    width: 40%;
}

.product-list-element .list-element-info .product-price p {
    display: inline;
    color: gray;
}

.product-list-element .list-element-info .product-price p:first-child {
    font-size: 25px;
}

.product-list-element .list-element-info .product-price p:last-child {
    font-size: 18px;
    font-weight: bold;
}

.bottom-line {
    position: relative;
    bottom: -50px;
    height: 1px;
    background-color: gray;
    opacity: 0.4;
}

.product-name p:hover {
    cursor: pointer;
    font-weight: 500;
}

</style>