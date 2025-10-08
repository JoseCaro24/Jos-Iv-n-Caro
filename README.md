<!--
  Archivo: portada_estudiante_riesgo.html
  Descripción: Portada/imagen de cabecera estilizada para un "Estudiante de Economía - Especialista en Riesgo".
  Instrucciones:
    1) Guarda este archivo en tu repo de GitHub (por ejemplo: /portada_estudiante_riesgo.html).
    2) Abre el archivo en el navegador o activa GitHub Pages en el repositorio para mostrarlo en web.
    3) Para cambiar la foto, reemplaza la URL en la variable --cover-image (línea indicada) o pon tu propia imagen local.
    4) Puedes editar los textos (nombre, título, universidad) directamente en el <header>.

  Nota: la imagen por defecto proviene de Unsplash (query libre). Si prefieres usar una foto propia, sube la imagen al repo y reemplaza la URL.
-->

<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Portada — Estudiante de Economía (Riesgo)</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;900&family=Merriweather:wght@700&display=swap" rel="stylesheet">
  <style>
    :root{
      --cover-image: url('https://source.unsplash.com/1600x900/?economics,finance,student,risk'); /* Reemplaza por tu imagen */
      --accent: rgba(10,25,47,0.85);
      --glass: rgba(255,255,255,0.06);
      --max-width: 1200px;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,system-ui,Segoe UI,Roboto,'Helvetica Neue',Arial}
    .cover{
      min-height:60vh;
      display:flex;
      align-items:center;
      justify-content:center;
      color:white;
      position:relative;
      overflow:hidden;
      background-image: var(--cover-image);
      background-size:cover;
      background-position:center center;
    }
    /* overlay gradient to improve contrast */
    .cover::before{
      content:'';position:absolute;inset:0;background:linear-gradient(180deg, rgba(0,0,0,0.25), rgba(0,0,0,0.55));backdrop-filter:blur(3px);
    }
    .container{
      position:relative;z-index:2;max-width:var(--max-width);padding:48px;width:100%;display:flex;gap:24px;align-items:center;
    }
    .card{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:18px;padding:28px;backdrop-filter: blur(6px);box-shadow:0 10px 30px rgba(2,6,23,0.45);display:flex;flex-direction:row;align-items:center;gap:24px;width:100%;
    }
    .avatar{
      width:160px;height:160px;border-radius:12px;flex:0 0 160px;overflow:hidden;border:3px solid rgba(255,255,255,0.12);
      background:linear-gradient(135deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));display:flex;align-items:center;justify-content:center;
    }
    .avatar img{width:100%;height:100%;object-fit:cover;display:block}
    .info{flex:1}
    .role{font-family:Merriweather,serif;font-size:28px;margin:0 0 6px 0}
    .name{font-weight:900;font-size:36px;margin:0;letter-spacing:-0.4px}
    .meta{margin-top:8px;color:rgba(255,255,255,0.85);font-size:15px}
    .badges{display:flex;gap:10px;margin-top:14px}
    .badge{padding:6px 10px;border-radius:999px;background:rgba(255,255,255,0.06);border:1px solid rgba(255,255,255,0.06);font-weight:600;font-size:13px}
    .actions{margin-left:auto;display:flex;gap:12px}
    .cta{background:transparent;border:1px solid rgba(255,255,255,0.14);padding:10px 14px;border-radius:10px;font-weight:700;color:white;text-decoration:none}

    /* responsive */
    @media (max-width:800px){
      .card{flex-direction:column;align-items:flex-start}
      .avatar{width:120px;height:120px}
      .name{font-size:24px}
      .role{font-size:20px}
      .actions{width:100%;justify-content:space-between}
    }

    /* footer small credit */
    .credit{position:absolute;right:18px;bottom:10px;color:rgba(255,255,255,0.6);font-size:12px;z-index:3}
  </style>
</head>
<body>
  <header class="cover" role="banner" aria-label="Portada Estudiante de Economía - Riesgo">
    <div class="container">
      <div class="card">
        <div class="avatar" aria-hidden="true">
          <!-- Avatar por defecto: puedes sustituir por tu foto (sube al repo y usa la ruta) -->
          <img src="https://source.unsplash.com/400x400/?portrait,student" alt="Retrato estudiante" />
        </div>
        <div class="info">
          <p class="role">Estudiante de Economía</p>
          <h1 class="name">[Tu Nombre] — Especialista en Riesgo</h1>
          <p class="meta">Universidad Nacional / Experiencia en análisis de riesgo de mercado, gestión de portafolios y modelado financiero.</p>
          <div class="badges">
            <span class="badge">Excel Avanzado</span>
            <span class="badge">Modelado Financiero</span>
            <span class="badge">Análisis de Riesgo</span>
          </div>
        </div>
        <div class="actions" aria-hidden="true">
          <a class="cta" href="#">Ver CV</a>
          <a class="cta" href="#">Contactar</a>
        </div>
      </div>
    </div>
    <div class="credit">Imagen: Unsplash · Diseño: plantilla HTML</div>
  </header>

  <main style="padding:40px;max-width:900px;margin:0 auto;">
    <h2 style="font-family:Merriweather,serif;margin-top:0">Cómo personalizar</h2>
    <ol>
      <li>Para cambiar la imagen de fondo: modifica la variable <code>--cover-image</code> en el <code>:root</code> (encabezado del CSS) o reemplaza la URL por la ruta de tu imagen.</li>
      <li>Para usar tu retrato en el avatar: sustituye la URL en el <code>&lt;img src=...&gt;</code> dentro de <code>.avatar</code> por la ruta de tu archivo.</li>
      <li>Edita el texto (nombre, universidad, descripciones) directamente en el HTML.</li>
      <li>Si quieres una imagen de alta calidad desde Unsplash con términos específicos, usa: <code>https://source.unsplash.com/1600x900/?economics,university,finance,risk</code></li>
      <li>Sube el archivo al repo y activa GitHub Pages (Settings → Pages) si quieres una URL pública.</li>
    </ol>

    <p>¿Quieres que genere una versión exportable (PNG) lista para usar como portada en LinkedIn o PDF? Si sí, dime el texto exacto (nombre, universidad, roles) y lo preparo en HTML listo para exportar.</p>
  </main>
</body>
</html>
