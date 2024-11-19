<template>
    <nav class="navbar">
      <ul>
        <li class="boton2"><NuxtLink to="/">Inicio</NuxtLink></li>
        <li class="boton2"><NuxtLink to="/contenido">Contenido</NuxtLink></li>
        <li class="boton2"><NuxtLink to="/quiz">Quiz</NuxtLink></li>
      </ul>
    </nav>
  </template>
  
  <script setup>
  // Barra de navegación
  </script>
  
  <style scoped>
  .navbar {
    background: linear-gradient(to right, #2c3e50, #3498db);
  padding: 1rem 0;
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }
  .navbar ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
  }
  .navbar li {
    margin: 0 10px;
  }
  .navbar a {
    color: white;
    text-decoration: none;
    font-weight: bold;
  }
  .navbar a:hover {
    border-radius: 15px;
    border: 3px solid #fff;
    padding: 5px;
  }
  </style>
