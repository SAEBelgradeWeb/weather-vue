<template>
    <div id="root">
        <router-link tag="li" to="/">
            <a>Today</a>
        </router-link>
        <router-link tag="li" to="/ten-days">
            <a>10 Days</a>
        </router-link>
        <router-view></router-view>
    </div>
</template>

<script>

  export default {
    name: 'app',

  }
</script>

<style>

</style>
