<!-- src/views/Tugas4.vue -->
<template>
    <div class="tugas">
      <h2>Tugas 4</h2>
      <p>Ini adalah halaman tugas 4.</p>
      <p><a :href="netlifyUrl" target="_blank">{{ netlifyUrl }}</a></p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        netlifyUrl: 'https://nadiaanakampun-223510190-tugas4.netlify.app/' // URL Netlify untuk Tugas 4
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
  