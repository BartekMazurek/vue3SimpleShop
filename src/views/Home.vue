<template>
    <div class="home">
        <div class="card">
            <div class="card-body">
                <h2 class="card-title">
                    Vue3 SimpleShop example
                </h2>
                <h6 class="card-subtitle mb-2 text-muted">
                    Author: Bartłomiej Mazurek
                </h6>
                <a href="" class="card-link">
                    LinkedIn
                </a>
                <a href="https://github.com/bartekmazurek" class="card-link">
                    GitHub
                </a>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Home',
    components: {}
}
</script>

<style scoped>
    .home .card {
        color: #ff5a00;
        border: 1px solid #ff5a00;
        border-radius: 0px;
    }

    .home .card-title {
        margin-bottom: 30px;
    }

    .home a {
        color: #ff5a00;
    }

    .home a:hover {
        text-decoration: underline;
        text-underline-offset: 5px;
    }
</style>
