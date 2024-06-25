<!-- src/views/Tugas3.vue -->
<template>
    <div class="tugas">
      <h2>Tugas 3</h2>
      <p>Ini adalah halaman tugas 3.</p>
      <p><a :href="netlifyUrl" target="_blank">{{ netlifyUrl }}</a></p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        netlifyUrl: 'https://tugas3pbk-223510190.netlify.app/' // URL Netlify untuk Tugas 3
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
  