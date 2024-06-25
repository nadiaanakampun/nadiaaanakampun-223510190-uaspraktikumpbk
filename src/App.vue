<template>
  <div id="app">
    <header>
      <h1>Weather Application</h1>
      <nav>
        <ul>
          <li class="dropdown">
            <button class="dropbtn">
              Tugas Nadia <i class="fas fa-chevron-down"></i>
            </button>
            <div class="dropdown-content">
              <a href="https://6610d19c6670f5952dc726ff--sage-dasik-77d8d4.netlify.app/" target="_blank">Tugas 1</a>
              <a href="https://nadiaanakampun-223510190-t2.netlify.app/" target="_blank">Tugas 2</a>
              <a href="https://tugas3pbk-223510190.netlify.app/" target="_blank">Tugas 3</a>
              <a href="https://nadiaanakampun-223510190-tugas4.netlify.app/" target="_blank">Tugas 4</a>
              <a href="https://nadiaanakampun-223510190-t5.netlify.app/products" target="_blank">Tugas 5</a>
              <a href="https://nadiaanakampun-223510190-tugas6pbk.netlify.app/" target="_blank">Tugas 6</a>
              <a href="https://main--nadiaanakampun-223510190-tugas7.netlify.app/" target="_blank">Tugas 7</a>
            </div>
          </li>
        </ul>
      </nav>
    </header>
    <WeatherWidget />
  </div>
</template>

<script>
import WeatherWidget from './components/WeatherWidget.vue';

export default {
  name: 'App',
  components: {
    WeatherWidget
  }
};
</script>

<style scoped>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');

body {
  margin: 0;
  font-family: 'Roboto', sans-serif;
  background-color: #f4f4f9;
}

#app {
  text-align: center;
  margin-top: 20px;
}

header {
  background-color: #1e3a5f;
  color: #fff;
  padding: 10px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

h1 {
  margin: 0;
  font-size: 24px;
  font-weight: 300;
  letter-spacing: 1px;
}

nav ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
}

nav ul li {
  position: relative;
}

.dropbtn {
  background-color: #1e3a5f;
  color: white;
  padding: 10px;
  font-size: 16px;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  transition: background-color 0.3s, transform 0.3s;
}

.dropbtn i {
  margin-left: 8px;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #ffffff;
  min-width: 160px;
  box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
  z-index: 1;
  border-radius: 4px;
  overflow: hidden;
  transition: opacity 0.3s ease;
  opacity: 0;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  transition: background-color 0.3s;
}

.dropdown-content a:hover {
  background-color: #f1f1f1;
}

.dropdown:hover .dropdown-content {
  display: block;
  opacity: 1;
}

.dropdown:hover .dropbtn {
  background-color: #145a8b;
  transform: translateY(-2px);
}

/* Weather Widget styles */
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
