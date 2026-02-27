# Proyecto de ejemplo: Tarea evaluativa práctica UF1842

Este repositorio contiene una pequeña página web estática diseñada para una tarea práctica de HTML y CSS. A continuación se describe la estructura del código, las clases utilizadas y su propósito.
aqui adjunto el enlace del diseño figma que se pretende conseguir: https://www.figma.com/design/GYGwdiG6jSahChdNHdEn0R/examen-UF1842?node-id=1-2&t=hz2mB0Ewjokr8INX-0


---

## Archivos principales

- `index.html`: documento HTML que define la estructura de la página.
- `css/reset.css`: hoja de estilo de "reset" de Meyer para normalizar estilos entre navegadores.
- `css/styles.css`: hoja de estilo con todas las reglas específicas del proyecto.

---

## `index.html`

El documento HTML es muy simple y se compone de los siguientes elementos clave:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tarea evaluativa práctica UF1842</title>
  <link rel="stylesheet" href="css/reset.css">
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <section class="hero">
    <div class="hero-content">
      <!-- Bloque de texto -->
      <div class="hero-text">
        <span class="badge">Inscripciones abiertas 2026</span>
        <h1 class="title">Construye tu futuro digital</h1>
        <p class="description">Domina HTML, CSS y herramientas modernas en una academia pensada para formar profesionales reales. Aprende con proyectos prácticos desde el primer día.</p>
      </div>
      <!-- Bloque de formulario -->
      <div class="hero-form">
        <form class="form" method="post">
          <input type="email" placeholder="tu email" required>
          <button type="submit">Empieza hoy</button>
        </form>
        <span class="stats">Únete a más de 5,000 estudiantes ya formados.</span>
      </div>
    </div>
  </section>
</body>
</html>
```

### Elementos y clases

- `<link rel="stylesheet" href="css/reset.css">`: referencia al archivo `reset.css` que resetea los estilos por defecto de los navegadores.
- `<link rel="stylesheet" href="css/styles.css">`: referencia al archivo con los estilos específicos.

- `<section class="hero">`: contenedor principal de la sección destacada o "hero".
- `<div class="hero-content">`: envoltorio interno que organiza el contenido en mobile y, mediante `grid`, en pantallas mayores.
- `<div class="hero-text">`: bloque de texto con título, descripción y distintivo (`badge`).
  - `<span class="badge">`: etiqueta de puntaje o anuncio, estilizada con fondo y mayúsculas.
  - `<h1 class="title">`: título principal.
  - `<p class="description">`: párrafo descriptivo.

- `<div class="hero-form">`: bloque que contiene el formulario de captura de email.
  - `<form class="form" method="post">`: formulario con clase `form` para aplicar estilos flexibles.
    - `<input type="email" placeholder="tu email" required>`: campo de email.
    - `<button type="submit">`: botón de envío.
  - `<span class="stats">`: texto con estadísticas/comentario adicional.

---

## `css/styles.css`

Contiene todas las reglas de estilo utilizadas en el proyecto. Se organizan de la siguiente manera:

1. **Variables CSS** (`:root`): define colores, tipografías y valores reutilizables.
2. **Reset/base**: aplica `box-sizing`, margin/padding cero, reglas para `body`.
3. **Estilos de la sección `.hero`**: max-width, padding, fondo, sombra, etc.
4. **Estilos de `.hero-content`**: comportamiento responsive (block por defecto, grid en escritorio).
5. **Clases de componentes**:
   - `.badge`: etiqueta redondeada con fondo azul/gris.
   - `.title`: tamaño y color del título.
   - `.description`: formato del párrafo.
   - `.form`: diseño flexible de formulario.
   - `.form input[type="email"]`: campos de entrada con estilos y focus.
   - `.form button`: botón primario con hover.
   - `.stats`: texto de estadísticas.
6. **Media queries**: adaptaciones para tabletas (768-1023px) y escritorio (≥1024px), ajustando tamaños, padding y disposición. En la versión de escritorio la hoja de estilos también cambia el fondo principal, cargando una ilustración SVG (`img/abstract-illustration.svg`) junto con la imagen de fondo JPG para enriquecer el diseño.

Cada regla está comentada en el archivo, proporcionando orientación sobre su propósito y contexto.

---

## Flujo y dependencias

- El HTML carga primero el reset y luego los estilos, asegurando que las personalizaciones no sean anuladas.
- Las clases se asignan en el HTML según su función visual; el CSS no contiene selectores complejos ni dependencias JS.
- Todos los colores y medidas se toman de las variables de `:root` para facilitar cambios globales.

---

## Uso

Abrir `index.html` en un navegador moderno mostrará la sección "hero" centrada con un formulario de inscripción. El diseño es responsivo y se adapta a móviles, tabletas y escritorio.

---

Este README proporciona un resumen para entender rápidamente la estructura y estilos del proyecto. 