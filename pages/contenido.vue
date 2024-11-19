<template>
  <div>
    <NavBar />
    <section class="hero">
      <h1>Introducción al Desarrollo Web</h1>
      <p>
        El desarrollo web es el arte de crear sitios y aplicaciones interactivas que funcionan en internet. 
        Combina diseño, programación y tecnología para brindar experiencias atractivas y funcionales a los usuarios.
      </p>
    </section>
    
    <section class="content">
      <div class="section">
        <h2>¿Qué es el Desarrollo Web?</h2>
        <p>
          Es el proceso de construir y mantener sitios web. Incluye tres áreas principales:
        </p>
        <ul>
          <li><strong>Frontend</strong>: Lo que los usuarios ven y con lo que interactúan (diseño, botones, animaciones).</li>
          <li><strong>Backend</strong>: La lógica y el almacenamiento detrás del sitio (servidores, bases de datos).</li>
          <li><strong>Full-stack</strong>: Una combinación de ambas.</li>
        </ul>
      </div>
      
      <div class="section">
        <h2>Lenguajes Esenciales</h2>
        <p>Estos son los pilares fundamentales para el desarrollo web:</p>
        <div class="languages">
          <div class="language-card">
            <h3>HTML</h3>
            <p>Define la estructura del sitio web mediante etiquetas. Por ejemplo, encabezados, párrafos y tablas.</p>
          </div>
          <div class="language-card">
            <h3>CSS</h3>
            <p>Estiliza la apariencia del sitio: colores, fuentes, diseño de las páginas y animaciones.</p>
          </div>
          <div class="language-card">
            <h3>JavaScript</h3>
            <p>Añade interactividad y lógica: ventanas emergentes, formularios dinámicos y más.</p>
          </div>
        </div>
      </div>
      
      <div class="section">
        <h2>Herramientas de Desarrollo</h2>
        <p>
          Los desarrolladores utilizan diferentes herramientas para crear sitios web. Algunas de las más populares incluyen:
        </p>
        <ul>
          <li>Frameworks de JavaScript: Vue.js, React, Angular.</li>
          <li>Control de versiones: Git y GitHub para colaborar y gestionar cambios.</li>
          <li>Editores de código: VS Code, Sublime Text, Atom.</li>
        </ul>
      </div>
      
      <div class="section">
        <h2>Buenas Prácticas</h2>
        <p>
          Para crear sitios web efectivos, sigue estas prácticas:
        </p>
        <ul>
          <li>Diseña pensando en el usuario: asegúrate de que sea fácil de usar.</li>
          <li>Optimiza para dispositivos móviles (diseño responsivo).</li>
          <li>Sigue estándares de accesibilidad para que todos puedan usar tu sitio.</li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script setup>
import NavBar from '~/components/NavBar.vue'
</script>

<style scoped>
/* Estilos para la página de contenido */
.hero {
  text-align: center;
  background: linear-gradient(135deg, #6a11cb, #2575fc);
  color: white;
  padding: 40px 20px;
  margin-bottom: 20px;
  border-radius: 10px;
  margin-top: 10px
}
.hero h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}
.hero p {
  font-size: 1.2rem;
}

.content {
  padding: 20px;
}

.section {
  margin-bottom: 40px;
}
.section h2 {
  font-size: 2rem;
  color: #333;
  border-bottom: 2px solid #6a11cb;
  display: inline-block;
  padding-bottom: 5px;
  margin-bottom: 15px;
}
.section p {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #555;
}
.section ul {
  list-style: square;
  margin-left: 20px;
}
.section ul li {
  font-size: 1.1rem;
  margin-bottom: 10px;
}

.languages {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}
.language-card {
  flex: 1 1 calc(33.333% - 20px);
  background: #f9f9f9;
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
.language-card h3 {
  color: #6a11cb;
  font-size: 1.5rem;
  margin-bottom: 10px;
}

</style>

  