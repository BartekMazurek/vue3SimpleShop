<template>

    <div class="product-list-element-details">
        Some details about product with id {{ productIdToShowDetails }} ...
    </div>

</template>

<script>

export default {
    name: "ProductListElementDetails",
    props: {
        productIdToShowDetails: Number
    }
}

</script>

<style scoped>

.product-list-element-details {
    width: 600px;
    height: 400px;
    position: absolute;
    top: 10%;
    left: 15%;
    margin: 0 auto;
    background-color: #FFFF;
    color: gray;
    border: 1px solid lightgrey;
    -webkit-box-shadow: 2px 2px 10px 0 rgba(0, 0, 0, 0.3);
    box-shadow: 2px 2px 10px 0 rgba(0, 0, 0, 0.3);
}

</style>