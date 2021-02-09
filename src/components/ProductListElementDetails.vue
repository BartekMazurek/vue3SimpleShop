<template>

    <div class="product-list-element-details">
        <div class="content-container">
            <h5>Description for product {{ productId }}</h5>
            {{ productDescription }}
        </div>
        <div class="close-window-row">
            <button @click="closeProductDetailsWindow">CLOSE</button>
        </div>
    </div>

</template>

<script>

export default {
    name: "ProductListElementDetails",
    props: {
        productId: {
            type: Number,
            required: true
        },
        productDescription: {
            type: String,
            required: true
        }
    },
    methods: {
        closeProductDetailsWindow() {
            this.$emit('closeProductDetailsWindow', false);
        }
    }
}

</script>

<style scoped>

.product-list-element-details {
    width: 840px;
    height: 600px;
    position: absolute;
    top: 0px;
    margin: 0 auto;
    background-color: #FFFF;
    color: gray;
    border: 1px solid lightgrey;
    -webkit-box-shadow: 2px 2px 10px 0 rgba(0, 0, 0, 0.3);
    box-shadow: 2px 2px 10px 0 rgba(0, 0, 0, 0.3);
}

.product-list-element-details .content-container {
    margin: 30px;
    height: 400px;
    max-height: 400px;
    overflow-x: auto;
}

.product-list-element-details .close-window-row {
    position: relative;
    bottom: -15%;
    left: 45%;
}

.product-list-element-details button {
    background-color: #ff5a00;
    color: #FFFF;
    border: 1px solid #ff5a00;
    height: 30px;
    margin-left: 10px;
    padding: 0px 10px 0px 10px;
    font-size: 14px;
    border-radius: 0px;
}

</style>