<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
  <div>
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" >
<link href="https://fonts.googleapis.com/css2?family=Libre+Bodoni:ital,wght@0,400..700;1,400..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
    <footer class="footer">
      <div class="footer-content">
        <img 
          class="footer-image" 
          src="https://th.bing.com/th/id/R.0cee4c4e109e44560fe5dcc2b6cf01fb?rik=boK9Vp1Gr6rJ1A&pid=ImgRaw&r=0" 
          alt="Logo del OVA"
        />
        <div class="footer-text">
          <p>
            &copy; 2024 OVA Introducción al Desarrollo Web. Todos los derechos reservados. 
          </p>
          <p>
            Este sitio web fue creado con fines educativos para explicar los fundamentos del desarrollo web. 
            El contenido no puede ser reproducido sin autorización.
          </p>
          <p>
            Creado por: Luis Blanchar y Edgar Zambrano
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
* {
  font-family: "Poppins";
}
.footer {
  background-color: #333;
  color: white;
  padding: 20px;
  margin-top: 20px;
}

.footer-content {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  max-width: 1200px;
  margin: 0 auto;
}

.footer-image {
  width: 80px;
  height: auto;
  margin-right: 20px;
  border-radius: 8px;
}

.footer-text {
  line-height: 1.6;
  text-align: left;
  font-size: 0.9rem;
}

.footer p {
  margin: 5px 0;
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .footer-image {
    margin-bottom: 10px;
    margin-right: 0;
  }
}
</style>


