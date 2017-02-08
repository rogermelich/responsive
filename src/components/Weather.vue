<template>
    <div class="weather">
        <div class="location">{{ location }}</div>
        <div class="date">{{ date }}</div>
        <div class="description">{{ description }}</div>
        <div class="current">
            <div class="visual">
                <div class="cloud">coud</div>
                <div class="temp">35</div>
                <div class="scale">º</div>
            </div>
            <div class="text">
                <div class="precipitation">Precipitation: {{ precipitation }}</div>
                <div class="humidity">Humidity: {{ humidity }}</div>
                <div class="wind">Wind: {{ wind }}</div>
                <div class="pollen">Pollen: {{ pollen }}</div>
            </div>
        </div>
        <div class="forecast">
            <div class="forecast-day" v-for="forecast in forecasts">
                <div class="date">{{ foreach.date }}</div>
                <div class="icon">{{ foreach.icon }}</div>
                <div class="low-temp">{{ foreach.low-temp }}</div>
                <div class="high-temp">{{ foreach.high-temp }}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'weather',
  data () {
    return {
       location: 'New York NY',
       date: 'Tuesday, April 15th',
       description: 'desc here',
       temp: 25,
       precipitation: '10%',
       humidity: '97%',
       wind: '4mph SW',
       pollen: '36',
       forecast: [
        {'date': 'Monday', 'icon': 'cloud', 'low-temp': 28, 'high-temp': 29},
        {'date': 'Tuesday', 'icon': 'sun', 'low-temp': 26, 'high-temp': 27},
        {'date': 'Wednesday', 'icon': 'sun-cloud', 'low-temp': 25, 'high-temp': 27},
        {'date': 'Thursday', 'icon': 'raining', 'low-temp': 26, 'high-temp': 29},
        {'date': 'Friday', 'icon': 'cloud', 'low-temp': 28, 'high-temp': 30},
        {'date': 'Saturday', 'icon': 'sun', 'low-temp': 30, 'high-temp': 32},
        {'date': 'Sunday', 'icon': 'thunder-storms', 'low-temp': 30, 'high-temp': 34}
       ]
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    .weather {
        padding: 25px;
    }
    .location {
        font-size: 3em;
    }
    .date {
        font-size: 1.5em;
    }
    .description {
        font-size: 1.1em;
    }
    .current {
        overflow: auto;
        width: 100%;
    }
    .visual {
        width: auto;
        float: right;
    }
    .text {
        width: auto;
        float: right;
    }
    .forecast-day {
        display: inline-block;
        width: 14.285%;
    }
    .icon.cloudy {
        background-image: url('../assets/cloudy.png');
    }

</style>
