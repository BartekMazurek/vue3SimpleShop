<template>

    <div class="container content-container">
        <div class="row">
            <div class="col-3">
                <filters></filters>
            </div>
            <div class="col-9">
                <search-bar></search-bar>
                <product-list></product-list>
            </div>
        </div>
    </div>

</template>

<script>

import SearchBar from "@/components/SearchBar";
import ProductList from "@/components/ProductList";
import Filters from "@/components/Filters";

export default {
    name: "Search",
    components: {
        Filters,
        ProductList,
        SearchBar
    }
}
</script>

<style scoped>
    .content-container .row > div:first-child {
        padding: 0px;
    }

    .content-container .row > div:nth-child(2) {
        padding-right: 0px;
    }
</style>
