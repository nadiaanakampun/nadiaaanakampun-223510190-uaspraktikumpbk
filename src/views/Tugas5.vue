<!-- src/views/Tugas5.vue -->
<template>
    <div class="tugas">
      <h2>Tugas 5</h2>
      <p>Ini adalah halaman tugas 5.</p>
      <p><a :href="netlifyUrl" target="_blank">{{ netlifyUrl }}</a></p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        netlifyUrl: 'https://nadiaanakampun-223510190-t5.netlify.app/products' // URL Netlify untuk Tugas 5
      };
    }
  };
  </script>
  
  <style scoped>
  .tugas {
    text-align: center;
    margin: 20px;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 8px;
    background-color: #fff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  </style>
  