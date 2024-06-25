<template>
  <div class="home">
    <h1>Welcome to Weather App</h1>
    <WeatherWidget />
    <router-link to="/assignment1">Assignment 1</router-link>
    <router-link to="/assignment2">Assignment 2</router-link>
  </div>
</template>

<script>
import WeatherWidget from '../components/WeatherWidget.vue';

export default {
  components: {
    WeatherWidget
  }
};
</script>

<style scoped>
.home {
  text-align: center;
  padding: 20px;
}
</style>
