# HTML5 — Apuntes para Obsidian

> [!info] Objetivo
> Aprender las etiquetas y conceptos fundamentales de HTML para crear la estructura de una página web.

## 1. ¿Qué es HTML?

**HTML** (*HyperText Markup Language*) es un **lenguaje de marcado**, no un lenguaje de programación. Sirve para estructurar el contenido de una web.

- **HTML:** estructura y contenido.
- **CSS:** apariencia y diseño.
- **JavaScript:** comportamiento e interactividad.

## 2. Estructura básica

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi página</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Hola, mundo</h1>
    <p>Mi primera web.</p>
</body>
</html>
```

| Elemento | Función |
|---|---|
| `<!DOCTYPE html>` | Indica que el documento utiliza HTML5. |
| `<html lang="es">` | Raíz del documento e idioma. |
| `<head>` | Metadatos y recursos, normalmente no visibles. |
| `<meta charset="UTF-8">` | Codificación de caracteres. |
| `<meta name="viewport" ...>` | Adaptación a dispositivos móviles. |
| `<title>` | Título de la pestaña. |
| `<link>` | Enlaza archivos externos como CSS. |
| `<body>` | Contenido visible de la página. |

> [!tip] VS Code
> Escribe `!` y pulsa **Tab** o **Enter** (Emmet) para generar la estructura básica.

## 3. Etiquetas de texto

| Etiqueta | Uso |
|---|---|
| `<h1>` a `<h6>` | Encabezados, del más importante al menos importante. |
| `<p>` | Párrafo. |
| `<strong>` | Texto con importancia especial. |
| `<em>` | Énfasis. |
| `<br>` | Salto de línea. |
| `<hr>` | Separación temática. |
| `<span>` | Contenedor de texto en línea. |
| `<small>` | Comentario o letra pequeña. |

```html
<h1>Elite Motors</h1>
<h2>Vehículos disponibles</h2>
<p>Encuentra tu próximo coche.</p>
<p><strong>Oferta:</strong> <em>últimas unidades</em>.</p>
```

## 4. Estructura semántica

Las etiquetas **semánticas** explican qué función cumple cada zona de la página.

| Etiqueta | Uso |
|---|---|
| `<header>` | Cabecera de página o sección. |
| `<nav>` | Navegación principal o secundaria. |
| `<main>` | Contenido principal (normalmente uno por página). |
| `<section>` | Sección temática, generalmente con encabezado. |
| `<article>` | Contenido independiente, como una ficha de producto. |
| `<aside>` | Información complementaria. |
| `<footer>` | Pie de página o sección. |
| `<div>` | Contenedor genérico sin significado semántico. |

```html
<header>
    <h1>Elite Motors</h1>
    <nav>
        <a href="index.html">Inicio</a>
        <a href="vehiculos.html">Vehículos</a>
    </nav>
</header>

<main>
    <section>
        <h2>Catálogo</h2>
        <article>
            <h3>BMW Serie 3</h3>
            <p>Precio: 29.900 €</p>
        </article>
    </section>
</main>

<footer><p>© 2026 Elite Motors</p></footer>
```

## 5. Enlaces e imágenes

### Enlaces (`<a>`)

```html
<a href="contacto.html">Contacto</a>
<a href="#catalogo">Ir al catálogo</a>
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Abrir otra web</a>
```

- `href`: destino.
- `target="_blank"`: abre otra pestaña o ventana.
- `rel="noopener noreferrer"`: protección y privacidad al abrir enlaces externos.
- `#catalogo`: apunta a un elemento con `id="catalogo"`.

### Imágenes (`<img>`)

```html
<img src="img/bmw.jpg" alt="BMW Serie 3 negro" width="400" height="250" loading="lazy">
```

- `src`: ruta de la imagen.
- `alt`: texto alternativo; importante para accesibilidad.
- `width` y `height`: dimensiones intrínsecas de la imagen.
- `loading="lazy"`: retrasa la carga de imágenes no prioritarias.

## 6. Listas

```html
<!-- Lista sin orden -->
<ul>
    <li>BMW</li>
    <li>Audi</li>
</ul>

<!-- Lista numerada -->
<ol>
    <li>Elegir coche</li>
    <li>Contactar</li>
</ol>
```

| Etiqueta | Uso |
|---|---|
| `<ul>` | Lista desordenada. |
| `<ol>` | Lista ordenada. |
| `<li>` | Elemento de lista. |

## 7. Formularios

Los formularios recogen datos. Para **procesarlos o guardarlos** se necesita un servidor o servicio adicional.

```html
<form action="/contacto" method="post">
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre" required>

    <label for="email">Correo:</label>
    <input type="email" id="email" name="email" required>

    <label for="marca">Marca:</label>
    <select id="marca" name="marca">
        <option value="bmw">BMW</option>
        <option value="audi">Audi</option>
    </select>

    <label for="mensaje">Mensaje:</label>
    <textarea id="mensaje" name="mensaje" rows="4"></textarea>

    <button type="submit">Enviar</button>
</form>
```

### Tipos frecuentes de `<input>`

| Tipo | Uso |
|---|---|
| `text` | Texto. |
| `email` | Correo electrónico. |
| `password` | Contraseña. |
| `number` | Número. |
| `tel` | Teléfono. |
| `date` | Fecha. |
| `checkbox` | Casilla independiente. |
| `radio` | Elegir una opción de un grupo. |
| `file` | Seleccionar archivo. |
| `search` | Campo de búsqueda. |

### Atributos de formularios

| Atributo | Uso |
|---|---|
| `name` | Nombre del dato enviado. |
| `value` | Valor del campo. |
| `required` | Campo obligatorio. |
| `placeholder` | Texto orientativo. |
| `min` / `max` | Límites numéricos o de fecha según el tipo. |
| `maxlength` | Longitud máxima. |
| `readonly` | Campo de solo lectura. |
| `disabled` | Campo deshabilitado, que no se envía con el formulario. |

> [!important] Accesibilidad
> Asocia cada `<label>` con su campo mediante `for` e `id`. El `placeholder` no sustituye a la etiqueta.

## 8. Tablas

Úsalas para **datos tabulares**, no para diseñar la distribución de la web.

```html
<table>
    <caption>Vehículos disponibles</caption>
    <thead>
        <tr><th scope="col">Modelo</th><th scope="col">Precio</th></tr>
    </thead>
    <tbody>
        <tr><td>BMW Serie 3</td><td>29.900 €</td></tr>
        <tr><td>Audi A4</td><td>27.500 €</td></tr>
    </tbody>
</table>
```

| Etiqueta | Uso |
|---|---|
| `<table>` | Tabla. |
| `<caption>` | Título descriptivo de la tabla. |
| `<thead>` | Encabezado. |
| `<tbody>` | Cuerpo. |
| `<tr>` | Fila. |
| `<th>` | Celda de encabezado. |
| `<td>` | Celda de datos. |

## 9. Atributos HTML importantes

| Atributo | Función |
|---|---|
| `id` | Identificador único dentro de la página. |
| `class` | Clase reutilizable para CSS y JavaScript. |
| `href` | Dirección de un enlace. |
| `src` | Ruta de un recurso. |
| `alt` | Alternativa textual de una imagen. |
| `title` | Información complementaria. |
| `lang` | Idioma del elemento o documento. |
| `style` | Estilos CSS en línea. |

### Diferencia entre `class` e `id`

```html
<article class="tarjeta">BMW</article>
<article class="tarjeta">Audi</article>
<section id="contacto">Contacta con nosotros</section>
```

```css
.tarjeta { border: 1px solid gray; } /* Clase */
#contacto { padding: 20px; }       /* ID */
```

## 10. Botones y navegación

```html
<button type="button">Mostrar información</button>
<button type="submit">Enviar formulario</button>
<a href="vehiculos.html">Ver vehículos</a>
```

- `<button>`: ejecuta una acción (normalmente con JavaScript) o envía un formulario.
- `<a>`: lleva a otra página o sección.

## 11. Vídeo y audio

```html
<video controls width="600" poster="img/portada.jpg">
    <source src="video/coche.mp4" type="video/mp4">
    Tu navegador no admite vídeo.
</video>

<audio controls>
    <source src="audio/presentacion.mp3" type="audio/mpeg">
    Tu navegador no admite audio.
</audio>
```

Atributos comunes: `controls`, `muted`, `loop`, `autoplay`. La reproducción automática puede estar bloqueada por el navegador.

## 12. Comentarios

```html
<!-- Cabecera principal -->
<header>...</header>
```

Los comentarios no se muestran en la página, pero son visibles en el código fuente. **No guardes secretos en ellos.**

## 13. Atajos Emmet (VS Code)

| Escribes | Genera |
|---|---|
| `!` | Plantilla HTML5. |
| `.tarjeta` | `<div class="tarjeta"></div>` |
| `#inicio` | `<div id="inicio"></div>` |
| `section.catalogo` | `<section class="catalogo"></section>` |
| `ul>li*3` | Lista con 3 elementos. |
| `h2+p` | Encabezado y párrafo. |
| `nav>a*4` | Navegación con 4 enlaces. |

## 14. Ejemplo: ficha de coche

```html
<article class="coche">
    <img src="img/bmw.jpg" alt="BMW Serie 3 negro" width="350" height="230">
    <h2>BMW Serie 3</h2>
    <p>BMW 320d automático</p>
    <ul>
        <li>Año: 2022</li>
        <li>Kilómetros: 35.000 km</li>
        <li>Combustible: diésel</li>
    </ul>
    <p><strong>29.900 €</strong></p>
    <a href="contacto.html">Solicitar información</a>
</article>
```

## 15. Buenas prácticas

1. Utiliza **HTML semántico** en lugar de llenar todo de `<div>`.
2. Mantén una jerarquía lógica de títulos (`h1`, `h2`, `h3`...).
3. Escribe textos `alt` útiles en imágenes informativas.
4. Asocia los campos de formulario con sus `<label>`.
5. Separa **HTML** (estructura) de **CSS** (presentación).
6. Usa enlaces para navegar y botones para acciones.
7. Comprueba la página en móvil y ordenador.
8. Indenta el código para facilitar su lectura.

