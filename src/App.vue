<template>
  <div id="app">
    <weather></weather>
  </div>
</template>

<script>
import Weather from './components/Weather'

export default {
  name: 'app',
  components: {
    Weather
  }
}
</script>

<style>

* {
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
body {
  font-family: Roboto, Arial;
  font-size: 1.2em;
  color: #888
}
</style>
