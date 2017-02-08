<template>
  <div id="app">
    <img src="./assets/logo.png">
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
  <!--border: 1px solid #999;-->
}

@media (min-width: 700px) {
  .weather {
    width: 700px;
  }
}

body {
    font-family: Roboto, Arial;
    font-size: 1.2ems;
    color: #666
}
</style>
