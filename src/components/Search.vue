<template>

    <div class="container">
        <div class="row">
            <div class="col-12">
                <search-bar></search-bar>
            </div>
        </div>
    </div>

    <div class="container">
        <div class="row">
            <div class="col-12">
                <product-list></product-list>
            </div>
        </div>
    </div>

</template>

<script>

import SearchBar from "@/components/SearchBar";
import ProductList from "@/components/ProductList";

export default {
    name: "Search",
    components: {
        ProductList,
        SearchBar
    }
}
</script>

<style scoped>

</style>
