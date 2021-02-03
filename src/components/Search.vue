<template>

    <div class="container content-container">
        <div class="row">
            <div class="col-3">
                <filters></filters>
            </div>
            <div class="col-9">
                <search-bar @searchQueryString="searchForProductsByQueryString($event)"></search-bar>
                <product-list :products="productsArray"></product-list>
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
    },
    data: () => ({
        productsArray: [
            {id: 1, name: 'Product1', description: 'Product1 description', price: 9.99},
            {id: 2, name: 'Product2', description: 'Product2 description', price: 10.},
            {id: 3, name: 'Product3', description: 'Product3 description', price: 15}
        ]
    }),
    methods: {
        searchForProductsByQueryString(event) {
            console.log(event);
        }
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
