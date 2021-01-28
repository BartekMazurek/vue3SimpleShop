<template>

    <div class="container">
        <div class="row">
            <div class="col-sm-12 col-md-6">
                Vue SimpleShop
            </div>
            <div class="col-sm-12 col-md-6">
                <navigation></navigation>
            </div>
        </div>
    </div>

    <div class="container">
        <div class="row">
            <div class="col-4">
                <filters></filters>
            </div>
            <div class="col-8">
                <router-view/>
            </div>
        </div>
    </div>

</template>

<style>


</style>

<script>

import Navigation from "@/components/Navigation";
import Filters from "@/components/Filters";

export default {
    components: {
        Filters,
        Navigation
    }
}

</script>