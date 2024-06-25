<template>
  <div class="weather-widget">
    <h2>Cuaca</h2>
    <input v-model="location" placeholder="Masukkan Lokasi" />
    <button @click="fetchWeather">
      <i class="fas fa-search"></i> Cari
    </button>
    <div v-if="weather" class="weather-info">
      <p><span>Lokasi:</span> {{ weather.name }}</p>
      <p><span>Suhu:</span> {{ weather.main.temp }} &deg;C</p>
      <p><span>Cuaca:</span> {{ weather.weather[0].description }}</p>
    </div>
    <div v-else>Loading data...</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      location: '',
      weather: null,
    };
  },
  methods: {
    async fetchWeather() {
      const apiKey = 'YOUR_API_KEY'; // Replace with your OpenWeatherMap API key
      const response = await fetch(
        `https://api.openweathermap.org/data/2.5/weather?q=${this.location}&units=metric&appid=${apiKey}`
      );
      const data = await response.json();
      this.weather = data;
    },
  },
};
</script>

<style scoped>
.weather-widget {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  max-width: 400px;
  margin: 20px auto;
  text-align: left;
  animation: fadeIn 0.5s ease;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.weather-widget h2 {
  font-size: 20px;
  margin-bottom: 10px;
  font-weight: 400;
  color: #333;
}

.weather-widget input {
  width: calc(100% - 60px);
  padding: 10px;
  margin-right: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  transition: border-color 0.3s;
}

.weather-widget input:focus {
  border-color: #1976d2;
  outline: none;
}

.weather-widget button {
  padding: 10px 20px;
  border: none;
  background-color: #1976d2;
  color: white;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.3s;
}

.weather-widget button:hover {
  background-color: #145a8b;
  transform: translateY(-2px);
}

.weather-widget button i {
  margin-right: 5px;
}

.weather-widget .weather-info {
  margin-top: 20px;
}

.weather-widget .weather-info p {
  margin: 5px 0;
  color: #333;
}

.weather-widget .weather-info p span {
  font-weight: bold;
}
</style>
