<template>
  <div>
    <NavBar />
    <section class="intro">
      <div class="header">
        <h1>¡Bienvenido a la Introducción al Desarrollo Web!</h1>
        <p>
          Aprende los conceptos básicos de desarrollo web utilizando herramientas modernas como <strong>Vue.js</strong>, <strong>Nuxt</strong>, y <strong>Vuetify</strong>. ¡Prepárate para explorar un mundo lleno de posibilidades!
        </p>
      </div>
      <div class="nav-buttons">
        <NuxtLink to="/contenido" class="btn">Comencemos</NuxtLink>
      </div>
      <div class="video-container">
        <video controls class="video" src="/components/Html.mp4.mp4"></video>
      </div>
    </section>
  </div>
</template>

<script setup>
import NavBar from '~/components/NavBar.vue'
</script>

<style scoped>
/* Fondo general */
body {
  font-family: 'Roboto', sans-serif;
  background-color: #f5f5f5;
  color: #333;
}
.nav-buttons {
    margin-top: 2rem;
    display: flex;
    justify-content: center;
  }
  
  .btn {
    padding: 15px 40px;
    border: none;
    outline: none;
    color: #000;
    cursor: pointer;
    position: relative;
    z-index: 0;
    border-radius: 12px;
    text-decoration: none;
    background-color: #fff;
    letter-spacing: 3px;
  }
  .btn:hover{
    content: "";
    background: linear-gradient(45deg,
    #6a11cb, #2575fc 
    );
    border: 3px solid #fff;
    color: #fff;
  }
  

  

/* Sección introductoria */
.intro {
  text-align: center;
  margin-top: 20px;
  padding: 40px 20px;
  background: linear-gradient(135deg, #6a11cb, #2575fc);
  color: white;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Encabezado */
.header h1 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  font-weight: bold;
}

.header p {
  font-size: 1.2rem;
  margin-bottom: 30px;
  line-height: 1.6;
}

/* Contenedor del video */
.video-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

/* Video */
.video {
  width: 80%;
  max-width: 800px;
  border: 2px solid white;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

/* Responsividad */
@media (max-width: 768px) {
  .header h1 {
    font-size: 1.8rem;
  }
  .header p {
    font-size: 1rem;
  }
  .video {
    width: 90%;
  }
}
</style>

  
  