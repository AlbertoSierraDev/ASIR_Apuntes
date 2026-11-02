# CSS3 — Apuntes básicos para Obsidian

> [!info] Objetivo
> Aprender qué es CSS, cómo conectarlo con HTML y cómo diseñar una web, por ejemplo, un concesionario de coches.

## 1. ¿Qué es CSS?

**CSS (Cascading Style Sheets)** es el lenguaje que define la apariencia de los elementos HTML: colores, tamaños, espacios, posiciones y adaptación a distintas pantallas.

- **HTML:** estructura y contenido.
- **CSS:** diseño y presentación.
- **JavaScript:** interactividad y comportamiento.

## 2. Cómo aplicar CSS a HTML

### Opción recomendada: archivo externo

Estructura de carpetas:

```text
concesionario/
├── index.html
├── css/
│   └── styles.css
└── img/
    └── coche.jpg
```

En el `<head>` de `index.html`:

```html
<link rel="stylesheet" href="css/styles.css">
```

En `css/styles.css`:

```css
body {
    background-color: #f5f5f5;
    color: #222;
    font-family: Arial, sans-serif;
}
```

**Importante:** la ruta de `href` es relativa al archivo HTML.

### Otras formas

**CSS interno**, dentro del `<head>`:

```html
<style>
    h1 { color: blue; }
</style>
```

**CSS en línea**, directamente en la etiqueta:

```html
<h1 style="color: blue;">Hola</h1>
```

Para proyectos, prefiere el **archivo externo** porque es más fácil de mantener.

## 3. Sintaxis de CSS

```css
selector {
    propiedad: valor;
    otra-propiedad: valor;
}
```

Ejemplo:

```css
h1 {
    color: darkblue;
    font-size: 32px;
}
```

- **Selector:** qué elemento modificar.
- **Propiedad:** qué aspecto cambiar.
- **Valor:** cómo debe quedar.
- `/* Comentario */` permite añadir notas.

## 4. Selectores más utilizados

| Selector | Ejemplo | Qué selecciona |
|---|---|---|
| Etiqueta | `p` | Todos los párrafos |
| Clase | `.tarjeta` | Elementos con `class="tarjeta"` |
| ID | `#inicio` | Elemento con `id="inicio"` |
| Descendiente | `.tarjeta p` | Párrafos dentro de `.tarjeta` |
| Hijo directo | `.menu > a` | Enlaces hijos directos de `.menu` |
| Varios | `h1, h2` | Ambos tipos de título |
| Pseudoclase | `a:hover` | Enlaces al pasar el ratón |

```html
<article class="tarjeta" id="coche-destacado">
    <h2>BMW Serie 3</h2>
</article>
```

```css
.tarjeta { padding: 20px; }
#coche-destacado { border: 2px solid black; }
.tarjeta h2 { color: navy; }
```

**Recuerda:** una `class` puede repetirse; un `id` debe ser único en la página.

## 5. Colores y fondos

```css
body {
    color: #222;                    /* Color del texto */
    background-color: #f2f2f2;     /* Color de fondo */
}

.portada {
    background-image: url("../img/coche.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
```

Los colores pueden escribirse como `red`, `#ff0000`, `rgb(255, 0, 0)` o `rgba(255, 0, 0, 0.5)`.

> [!tip] Rutas de imágenes en CSS
> `url("../img/coche.jpg")` se interpreta **desde la ubicación del archivo CSS**, no desde el HTML.

## 6. Texto y tipografía

| Propiedad | Para qué sirve |
|---|---|
| `font-family` | Tipo de letra |
| `font-size` | Tamaño de letra |
| `font-weight` | Grosor (`400`, `700`, `bold`) |
| `text-align` | Alineación (`left`, `center`, `right`) |
| `line-height` | Separación entre líneas |
| `text-decoration` | Subrayado, etc. |
| `letter-spacing` | Espacio entre letras |

```css
h1 {
    font-size: 36px;
    font-weight: 700;
    text-align: center;
}

p { line-height: 1.6; }
a { text-decoration: none; }
```

## 7. Medidas más habituales

| Unidad | Significado |
|---|---|
| `px` | Píxeles CSS |
| `%` | Porcentaje respecto a una referencia (según la propiedad) |
| `rem` | Relativa al tamaño de letra del elemento raíz |
| `em` | Relativa al tamaño de letra del elemento (según la propiedad) |
| `vw` | 1 % del ancho de la ventana |
| `vh` | 1 % del alto de la ventana |

```css
.contenedor {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}
```

## 8. Modelo de caja (Box Model)

Cada elemento tiene:

1. **Content:** contenido.
2. **Padding:** espacio interior.
3. **Border:** borde.
4. **Margin:** espacio exterior.

```css
* { box-sizing: border-box; }

.tarjeta {
    width: 300px;
    padding: 20px;
    border: 1px solid #ccc;
    margin: 16px;
    border-radius: 10px;
}
```

Con `box-sizing: border-box`, el ancho declarado incluye el `padding` y el borde.

Atajos:

```css
margin: 10px;             /* Todos los lados */
padding: 10px 20px;       /* Arriba/abajo y derecha/izquierda */
margin: 10px 20px 30px 40px; /* Arriba, derecha, abajo, izquierda */
```

## 9. Display y posicionamiento

| Propiedad | Uso |
|---|---|
| `display: block` | Ocupa una línea y normalmente todo el ancho disponible |
| `display: inline` | Sigue el flujo del texto |
| `display: inline-block` | En línea, pero permite dimensiones |
| `display: none` | Oculta el elemento y elimina su espacio |
| `position: relative` | Permite desplazarlo respecto a su posición normal |
| `position: absolute` | Lo posiciona respecto a su ancestro posicionado más cercano |
| `position: fixed` | Lo fija respecto a la ventana |
| `position: sticky` | Se adhiere al desplazarse, según un umbral |

```css
.menu { position: sticky; top: 0; }
```

## 10. Flexbox: colocar elementos en una fila o columna

Se aplica al **contenedor padre**.

```html
<nav class="menu">
    <a href="index.html">Inicio</a>
    <a href="vehiculos.html">Vehículos</a>
    <a href="contacto.html">Contacto</a>
</nav>
```

```css
.menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
}
```

| Propiedad | Función |
|---|---|
| `display: flex` | Activa Flexbox |
| `flex-direction` | Dirección: `row` o `column` |
| `justify-content` | Distribución en el eje principal |
| `align-items` | Alineación en el eje transversal |
| `gap` | Espacio entre elementos |
| `flex-wrap: wrap` | Permite saltar a otra línea |

## 11. CSS Grid: crear cuadrículas

Muy útil para el catálogo de coches.

```css
.catalogo {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
}
```

- `1fr`: una fracción del espacio disponible.
- `repeat(3, 1fr)`: tres columnas iguales.
- `gap`: separación entre tarjetas.

Versión adaptable sin definir un número fijo de columnas:

```css
.catalogo {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(100%, 250px), 1fr));
    gap: 24px;
}
```

## 12. Imágenes, botones y efectos

```css
.tarjeta img {
    display: block;
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
}

.boton {
    display: inline-block;
    background: #111;
    color: white;
    padding: 12px 20px;
    border-radius: 6px;
    text-decoration: none;
    transition: background-color 0.2s ease;
}

.boton:hover { background: #444; }
.boton:focus-visible { outline: 3px solid orange; }
```

- `object-fit: cover`: rellena el espacio recortando la imagen si es necesario.
- `transition`: suaviza cambios de propiedades.
- `:hover`: estilo al pasar el ratón.
- `:focus-visible`: muestra el foco al navegar con teclado.

## 13. Responsive: adaptar la web a móviles

Las **media queries** permiten cambiar estilos según el tamaño de pantalla.

```css
.catalogo {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

@media (max-width: 768px) {
    .catalogo {
        grid-template-columns: 1fr;
    }
}
```

En HTML incluye:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## 14. Cascada, especificidad y herencia

Si varias reglas afectan a un elemento, CSS decide cuál se aplica según su **origen, importancia, capa, especificidad y orden**, entre otros factores.

Regla práctica para estilos normales del mismo origen y capa:

- Un selector por **ID** suele tener más especificidad que uno por **clase**.
- Uno por **clase** suele tener más que uno por **etiqueta**.
- Si la especificidad empata, suele ganar la regla que aparece después.
- Algunas propiedades, como `color` y `font-family`, se heredan.

```css
p { color: black; }
.aviso { color: red; } /* Gana para <p class="aviso"> */
```

Evita abusar de `!important`.

## 15. Ejemplo completo: tarjeta de coche

**index.html**:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elite Motors</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header class="cabecera">
        <h1>Elite Motors</h1>
    </header>

    <main class="contenedor">
        <h2>Vehículos disponibles</h2>
        <section class="catalogo" aria-label="Catálogo de coches">
            <article class="tarjeta">
                <img src="img/coche.jpg" alt="BMW Serie 3 negro">
                <h3>BMW Serie 3</h3>
                <p>2022 · 35.000 km · Diésel</p>
                <p class="precio">29.900 €</p>
                <a class="boton" href="contacto.html">Solicitar información</a>
            </article>
        </section>
    </main>
</body>
</html>
```

**css/styles.css**:

```css
* { box-sizing: border-box; }

body {
    margin: 0;
    background: #f4f5f7;
    color: #222;
    font-family: Arial, sans-serif;
}

.cabecera {
    padding: 24px;
    background: #111827;
    color: white;
    text-align: center;
}

.contenedor {
    width: 90%;
    max-width: 1100px;
    margin: 40px auto;
}

.catalogo {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(100%, 260px), 1fr));
    gap: 24px;
}

.tarjeta {
    padding: 18px;
    background: white;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.tarjeta img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    border-radius: 8px;
}

.precio { font-size: 24px; font-weight: bold; }

.boton {
    display: inline-block;
    padding: 12px 16px;
    background: #111827;
    color: white;
    text-decoration: none;
    border-radius: 6px;
}

.boton:hover { background: #374151; }
.boton:focus-visible { outline: 3px solid #f59e0b; }
```

> [!warning] Para que se vea la imagen
> Guarda una imagen con el nombre `coche.jpg` dentro de `img/`. El enlace a `contacto.html` solo funcionará cuando crees esa página.

## 16. Errores comunes

| Problema | Qué comprobar |
|---|---|
| No se aplica el CSS | Ruta del `<link>`, nombre del archivo y extensión `.css` |
| No funciona una clase | Escribe `.nombre-clase`, no `nombre-clase` |
| No funciona un ID | Escribe `#nombre-id` |
| No aparece una imagen de fondo | Ruta relativa al archivo CSS |
| Un estilo no cambia | Comprueba especificidad y reglas posteriores |
| Se desborda la página | Revisa anchuras, `padding`, `box-sizing` y elementos sin ajuste |
| El móvil se ve mal | Revisa `viewport`, Grid/Flexbox y media queries |

## 17. Chuleta rápida de propiedades

| Propiedad | Función |
|---|---|
| `color` | Color del texto |
| `background-color` | Color del fondo |
| `font-size` | Tamaño del texto |
| `font-family` | Fuente |
| `font-weight` | Grosor del texto |
| `width` / `height` | Ancho / alto |
| `max-width` | Ancho máximo |
| `margin` | Espacio exterior |
| `padding` | Espacio interior |
| `border` | Borde |
| `border-radius` | Esquinas redondeadas |
| `box-shadow` | Sombra |
| `display` | Modo de distribución |
| `gap` | Espacio entre elementos de Flexbox/Grid |
| `justify-content` | Distribución en el eje principal de Flexbox |
| `align-items` | Alineación transversal en Flexbox |
| `grid-template-columns` | Columnas de Grid |
| `object-fit` | Ajuste de imágenes y vídeos |
| `transition` | Transición entre estilos |
