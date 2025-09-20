# red_social
explicacion de como se conforma el codigo de una pagina HTML5 para una red social
1.Diseño de HTML5 en los iconos  llamamos links Bootstrap Icons
   <!-- Bootstrap CSS -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
<!-- Bootstrap Icons -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.1/font/bootstrap-icons.css" rel="stylesheet">
1.1 configuramos los iconos (inicio, perfil, muro, mensajes)
<nav class="navigation">
    <input type="checkbox" id="nav-button">
    <label for="nav-button" onclick></label>
    <ul class="nav-container">
        <!-- Icono Inicio -->
        <div class="col-6 col-md-2">
        <a href="#inicio" id="inicio01" class="text-decoration-none text-dark d-flex flex-column align-items-center">
        <i class="bi bi-house-door-fill fs-1 mb-2"></i>
       <span>Inicio</span>
       </a>
       </div>
      <!-- Icono Perfil -->
      <div class="col-6 col-md-2">
      <a href="#perfil" id="perfil01" class="text-decoration-none text-dark d-flex flex-column align-items-center">
      <i class="bi bi-person-circle fs-1 mb-2"></i>
      <span>Perfil</span>
      </a>
      </div>
      <!-- Icono Muro -->
      <div class="col-6 col-md-2">
      <a href="#muro" id="muro01" class="text-decoration-none text-dark d-flex flex-column align-items-center">
      <i class="bi bi-collection-fill fs-1 mb-2"></i>
      <span>Muro</span>
      </a>
      </div>
      <!-- Icono Mensajes -->
      <div class="col-6 col-md-2">
      <a href="#mensajes" id="mensajes01" class="text-decoration-none text-dark d-flex flex-column align-items-center">
      <i class="bi bi-chat-dots-fill fs-1 mb-2"></i>
      <span>Mensajes</span>
      </a>
      </div>
    </ul>
</nav>
