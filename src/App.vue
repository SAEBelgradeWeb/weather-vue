<template>
    <div id="app">
       <navigation></navigation>
        <current-weather></current-weather>
        <hourly-weather></hourly-weather>
    </div>
</template>

<script>
  import Navigation from './Navigation.vue'
  import CurrentWeather from './CurrentWeather.vue'
  import HourlyWeather from './HourlyWeather.vue'
  export default {
    name: 'app',
    components: {
      Navigation, CurrentWeather, HourlyWeather
    }
  }
</script>

<style>

</style>
