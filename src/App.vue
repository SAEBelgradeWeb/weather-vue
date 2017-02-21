<template>
    <div id="app">
        <h1>{{ weather.main.temp | round }}</h1>
    </div>
</template>

<script>
  import axios from  'axios'
  export default {
    name: 'app',
    data() {
      return {
        weather: {
          main: {
            temp: ""
          }
        }
      }
    },
    filters: {
      round: function (input) {
        return Math.round(input)
      },
    },
    created() {
      let that = this;
      axios.get('http://api.openweathermap.org/data/2.5/weather',
          {
            params: {
              appid: 'b138aca5f679afcd22a1961e66aa5709',
              q: 'Belgrade,RS',
              units: 'metric'
            }
          }).then(function (response) {
        that.weather = response.data
        console.log(that.weather)
      })
    }

  }
</script>

<style>

</style>
