<template>

    <div class="container navigation-container">
        <div class="row top-row">
            <div class="col-sm-12 col-md-6">
                <h1 class="shop-name">simpleShop</h1>
            </div>
            <div class="col-sm-12 col-md-6">
                <navigation></navigation>
            </div>
        </div>
    </div>

    <div class="container content-container">
        <div class="row">
            <div class="col-12">
                <router-view/>
            </div>
        </div>
    </div>

</template>

<style scoped>

.top-row {
    margin-top: 10px;
    border: 1px solid #ff5a00;
}

.top-row > div:first-child,
.top-row > div:nth-child(2) {
    padding: 30px;
}

.shop-name {
    color: #ff5a00;
    font-weight: 800;
}

.content-container .row > div:first-child {
    margin-top: 20px;
    padding: 0px;
}

</style>

<script>

import Navigation from "@/components/Navigation";

export default {
    components: {
        Navigation
    }
}

</script>