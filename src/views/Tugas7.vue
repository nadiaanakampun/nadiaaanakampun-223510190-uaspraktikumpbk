<!-- src/views/Tugas7.vue -->
<template>
    <div class="tugas">
      <h2>Tugas 7</h2>
      <p>Ini adalah halaman tugas 7.</p>
      <p><a :href="netlifyUrl" target="_blank">{{ netlifyUrl }}</a></p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        netlifyUrl: 'https://main--nadiaanakampun-223510190-tugas7.netlify.app/' // URL Netlify untuk Tugas 7
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
  