# red_social
explicacion de como se conforma el codigo de una pagina HTML5 para una red social
1.Diseño de HTML5 en los iconos  llamamos links Bootstrap Icons
-Meta tags completos para SEO y accesibilidad
-Semántica HTML5 correcta con <header>, <nav>, <section>, <footer>
-ARIA labels para mejor accesibilidad
-Preload de recursos críticos para mejor rendimiento
-Favicon SVG optimizado
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


2.Aplicar estilos modernos con CSS3 y frameworks como TailwindCSS o Bootstrap.
-Gradientes avanzados con linear-gradient y radial-gradient
-Animaciones suaves con cubic-bezier y transition
-Efectos de hover con transformaciones y escalado
-Sombras modernas con box-shadow multicapa
-Backdrop filters para efectos de cristal
 <!-- Preload critical resources -->
 <link rel="preload" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" as="style">
 <link rel="preload" href="style.css" as="style">
 
 <!-- Stylesheets -->
 <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap">
 <link rel="stylesheet" href="style.css">
 <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
 
 <!-- Favicon -->
 <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🎓</text></svg>">
 

 <!-- Theme Color -->
 <meta name="theme-color" content="#ba66ea">

 3.Sistema de Grid Responsivo:
-CSS Grid para layouts complejos
-Flexbox para alineación y distribución
-Media queries optimizadas para móviles y tablets
-Menú hamburguesa animado para móviles
/* Reset and Base Styles */
*, *:before, *:after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f8f9fa;
    font-size: 1em;
    font-weight: normal;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Grid System */
.grid {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: 20px;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.col-1-1 {
    grid-column: span 12;
}

.col-1-2 {
    grid-column: span 6;
}

.col-1-3 {
    grid-column: span 4;
}

.col-1-4 {
    grid-column: span 3;
}

.grid-pad {
    padding: 40px 0;
}

/* Header Styles */
#top-header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    box-shadow: 0 2px 20px rgba(0,0,0,0.1);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    backdrop-filter: blur(10px);
}

.header-home {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
}

.logo-wrap {
    display: flex;
    align-items: center;
}

.logo {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: white;
    font-size: 1.5rem;
    font-weight: 700;
    transition: all 0.3s ease;
}

    .logo:hover {
        transform: scale(1.05);
    }

.brand-icon {
    width: 32px;
    height: 32px;
    margin-right: 0.5rem;
}

/* Navigation */
.navigation {
    position: relative;
}

    .navigation input[type="checkbox"] {
        display: none;
    }

    .navigation label {
        display: none;
        flex-direction: column;
        cursor: pointer;
        padding: 0.5rem;
    }

        .navigation label span {
            width: 25px;
            height: 3px;
            background: white;
            margin: 3px 0;
            transition: all 0.3s ease;
            border-radius: 2px;
        }

.nav-container {
    display: flex;
    list-style: none;
    gap: 2rem;
    margin: 0;
    padding: 0;
}

    .nav-container li {
        position: relative;
    }

    .nav-container a {
        color: white;
        text-decoration: none;
        padding: 0.5rem 1rem;
        border-radius: 20px;
        transition: all 0.3s ease;
        font-weight: 500;
        position: relative;
    }

        .nav-container a:hover,
        .nav-container a.current {
            background: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }

        .nav-container a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 50%;
            width: 0;
            height: 2px;
            background: #ffd700;
            transition: all 0.3s ease;
            transform: translateX(-50%);
        }

        .nav-container a:hover::after,
        .nav-container a.current::after {
            width: 80%;
        }

4.Implementar enlaces internos y externos.
<<?php
session_start();
if (!isset($_SESSION['username'])) {
    header("Location: http://localhost/pagina2/for.php");
    exit();
}
?>
            <form action="login.php" method="POST">
                <div class="input-group form-group">
                    <div class="input-group-prepend">
                        <span class="input-group-text"><i class="fas fa-user"></i></span>
                    </div>
                    <input type="text" name="username" class="form-control" placeholder="Usuario" required>
                </div>
                <div class="input-group form-group">
                    <div class="input-group-prepend">
                        <span class="input-group-text"><i class="fas fa-key"></i></span>
                    </div>
                    <input type="password" name="password" class="form-control" placeholder="Contraseña" required>
                </div>
                <div class="form-group">
                    <input type="submit" value="Login" class="btn float-right login_btn">
                </div>
            </form>
        </div>
        <div class="card-footer">
            <div class="d-flex justify-content-center links">
                ¿No tienes cuenta?
                <a href="#" id="showRegister">Regístrate</a>
            </div>
        </div>
    </div>
</div>
if ($stmt->execute()) {
    echo "<script>alert('Usuario registrado correctamente');window.location.href='for.php';</script>";
} else {
    echo "Error al registrar: " . $stmt->error;
}
