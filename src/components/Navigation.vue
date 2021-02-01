<template>
  <div class="navigation-bar">
    <router-link to="/">Home</router-link>
    <router-link to="/search">Search</router-link>
  </div>
</template>

<script>

export default {
  name: "Navigation"
}

</script>

<style scoped>

.navigation-bar a {
    color: #ff5a00;
    padding: 10px;
    font-size: 2rem;
    text-underline-offset: 13px;
}

.navigation-bar a:hover {
    font-weight: 500;
}

</style>