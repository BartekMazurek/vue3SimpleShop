<template>
    <div class="search-bar">
        <div class="content">
            <input type="text" placeholder="Search for products ..." v-model="queryString">
            <button class="btn" @click="searchProductByQueryString">SEARCH</button>
        </div>
    </div>
</template>

<script>

export default {
    name: "SearchBar",
    data: () => ({
        queryString: ''
    }),
    methods: {
        searchProductByQueryString() {
            this.$emit('searchQueryString', this.queryString);
        }
    }
}

</script>

<style scoped>

.search-bar {
    height: 100px;
    border: 1px solid #ff5a00;
    display: flex;
}

.search-bar .content {
    margin: 30px auto 0;
}

.search-bar input[type="text"],
.search-bar input[type="text"]:focus,
.search-bar input[type="text"]:active {
    font-size: 14px;
    color: gray;
    height: 30px;
    width: 400px;
    border: 1px solid lightgray;
    border-radius: 0px;
    -webkit-box-shadow: none !important;
    -moz-box-shadow: none !important;
    box-shadow: none !important;
    outline: none;
}

.search-bar button {
    background-color: #ff5a00;
    color: #FFFF;
    border: 1px solid #ff5a00;
    height: 30px;
    margin-left: 10px;
    padding: 0px 10px 0px 10px;
    font-size: 14px;
    border-radius: 0px;
}

.search-bar button:focus,
.search-bar button:active {
    -webkit-box-shadow: none !important;
    -moz-box-shadow: none !important;
    box-shadow: none !important;
}

</style>