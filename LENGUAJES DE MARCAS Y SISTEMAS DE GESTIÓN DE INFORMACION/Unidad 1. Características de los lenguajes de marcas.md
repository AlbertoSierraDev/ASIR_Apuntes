# 1. Lenguajes de marcas

Un lenguaje de marcas utiliza etiquetas o símbolos para añadir información sobre la estructura, el significado o la presentación de un texto.

## Características
- Permite estructurar y organizar información.
- Utiliza marcas o etiquetas.
- Añade información al contenido original.
- Sigue unas reglas de marcado.
- Facilita la interpretación e intercambio de documentos.

## Diferencia con los lenguajes de programación
Los lenguajes de programación ejecutan instrucciones y operaciones, mientras que los lenguajes de marcas describen y estructuran información.

**Ejemplos:** HTML y XML.

## A. Tipos de lenguajes de marcas

Los **lenguajes de marcas** se clasifican según su finalidad en cuatro tipos:

1. De presentación.
    
2. De procedimiento.
    
3. Descriptivos o semánticos.
    
4. Ligeros (LML).
    

## 1. Lenguajes de marcas de presentación

Son aquellos que **establecen el formato y la apariencia visual del texto**, es decir, cómo lo verá el usuario.

Permiten definir características como:

- Negrita y cursiva.
    
- Tamaño y tipo de letra.
    
- Colores y otros aspectos visuales.
    

**Ejemplos:** formatos de documentos utilizados por Microsoft Word, LibreOffice y OnlyOffice.

**Idea clave:** determinan cómo se presenta visualmente la información.

## 2. Lenguajes de marcas de procedimiento

Son lenguajes que **indican al programa las acciones que debe realizar para presentar un texto**.

**Características:**

- Se utilizan para controlar la presentación del contenido.
    
- El programa interpreta las instrucciones de marcado.
    
- Las instrucciones se procesan en el orden en el que aparecen.
    

**Ejemplos del temario:** HTML y LaTeX.

**Idea clave:** indican qué acciones debe realizar el programa para mostrar el contenido.

> [!NOTE] Aclaración  
> Aunque el temario incluye HTML en esta categoría, HTML moderno se utiliza principalmente para definir la estructura y el significado del contenido web.

## 3. Lenguajes de marcas descriptivos o semánticos

Son aquellos que **describen el significado y la estructura de la información**, sin determinar necesariamente cómo debe visualizarse.

**Características:**

- Identifican el significado de cada elemento.
    
- Organizan los datos mediante etiquetas.
    
- Separan la información de su presentación visual.
    

**Ejemplos:** XML y SGML.

**Ejemplo XML:**

```
<alumno>
    <nombre>Alberto</nombre>
    <curso>ASIR</curso>
    <nota>9</nota>
</alumno>
```

Cada etiqueta describe el significado de un dato, pero no establece su apariencia visual.

**Idea clave:** describen qué significa la información, no cómo debe verse.

## 4. Lenguajes de marcas ligeros (LML)

Son lenguajes que utilizan **una sintaxis sencilla para dar formato y estructurar documentos de texto**.

**Características:**

- Son fáciles de escribir y leer.
    
- Utilizan marcas simples.
    
- Se pueden editar con cualquier editor de texto.
    
- Los archivos de texto plano suelen ocupar poco espacio.
    
- Son útiles para documentación y apuntes.
    

**Ejemplos:** Markdown, reStructuredText y Textile.

**Ejemplo Markdown:**

```
# Título principal
## Subtítulo
**Texto en negrita**
- Elemento de una lista
```

Markdown es el lenguaje que utiliza Obsidian para dar formato a los apuntes.

**Idea clave:** permiten escribir documentos estructurados de manera rápida y sencilla.

---

## Tabla comparativa

|Tipo|Función principal|Ejemplos|
|---|---|---|
|Presentación|Define cómo se ve el texto.|Formatos de Word y LibreOffice|
|Procedimiento|Indica instrucciones de presentación.|LaTeX, HTML (según temario)|
|Descriptivo o semántico|Describe el significado de los datos.|XML, SGML|
|Ligero (LML)|Facilita la escritura de documentos.|Markdown, Textile|

## Resumen para el examen

> [!IMPORTANT] Conceptos que debes memorizar
> 
> - **Presentación:** cómo se ve el texto.
>     
> - **Procedimiento:** qué acciones se realizan para mostrarlo.
>     
> - **Descriptivo:** qué significa la información.
>     
> - **Ligero:** cómo escribir y estructurar texto fácilmente.
>     

**La diferencia principal entre los cuatro tipos es la finalidad para la que se utilizan las marcas.**

## B. Características de los lenguajes de marcas

Los **lenguajes de marcas** presentan una serie de características generales que permiten estructurar, describir y representar información.

## 1. Independencia del software

Los documentos suelen ser archivos de **texto plano**, por lo que pueden abrirse y editarse con diferentes programas, independientemente del software utilizado para crearlos.

**Ejemplo:** un archivo XML puede abrirse con el Bloc de notas, Visual Studio Code u Obsidian.

## 2. Marcas insertadas en el contenido

Las **etiquetas o marcas se encuentran dentro del propio documento**, junto con la información que describen.

**Ejemplo en XML:**

```
<nombre>Alberto</nombre>
<curso>ASIR</curso>
```

Las etiquetas `<nombre>` y `<curso>` forman parte del documento y permiten identificar los datos.

## 3. Sencillez y facilidad de uso

Los lenguajes de marcas utilizan **elementos sencillos e intuitivos** para organizar la información.

Además, permiten crear lenguajes específicos adaptados a diferentes necesidades.

**Ejemplo:** XML permite definir etiquetas personalizadas como `<alumno>`, `<profesor>` o `<asignatura>`.

## 4. Versatilidad y amplio uso

Los lenguajes de marcas son **muy versátiles**, ya que se utilizan en numerosos ámbitos.

**Principales aplicaciones:**

- **Páginas web:** estructuración del contenido mediante HTML.
    
- **Libros y documentos:** organización y presentación de textos.
    
- **Gráficos:** representación de imágenes vectoriales mediante SVG.
    
- **Fórmulas matemáticas:** representación mediante MathML.
    
- **Vídeos y contenido multimedia:** descripción de información y metadatos.
    
- **Sindicación de contenidos:** distribución de noticias y actualizaciones mediante RSS.
    

---

## Resumen para el examen

> [!IMPORTANT] Características principales
> 
> 1. **Independencia:** documentos de texto plano editables con diferentes programas.
>     
> 2. **Marcas integradas:** las etiquetas están insertadas en el contenido.
>     
> 3. **Sencillez:** utilizan elementos intuitivos y permiten crear lenguajes específicos.
>     
> 4. **Versatilidad:** se utilizan en páginas web, documentos, gráficos, matemáticas y contenidos multimedia.
>     

**Idea clave:** los lenguajes de marcas permiten representar y organizar información de forma sencilla, flexible y compatible con diferentes herramientas.
# 2. Conceptos básicos de los lenguajes de marcas

Los lenguajes de marcas utilizan diferentes componentes para estructurar y describir la información de un documento.

Los principales son:

1. **Etiquetas o marcas.**
    
2. **Elementos.**
    
3. **Atributos.**
    
4. **Metadatos.**
    

## A. Etiquetas o marcas

Las **etiquetas** son códigos que se añaden al texto para indicar su estructura, significado o presentación.

Cada lenguaje de marcas tiene sus propias etiquetas y reglas.

### Tipos de etiquetas

|Tipo|Función|Ejemplo|
|---|---|---|
|Apertura|Indica el comienzo de un elemento.|`<p>`|
|Cierre|Indica el final de un elemento.|`</p>`|
|Vacía|Representa un elemento sin contenido.|`<br>`|

**Ejemplo HTML:**

```
<p>Contenido del párrafo</p>
```

- `<p>`: etiqueta de apertura.
    
- `Contenido del párrafo`: contenido.
    
- `</p>`: etiqueta de cierre.
    

### Características

- Las etiquetas forman parte del código, no del contenido textual.
    
- En HTML se recomienda escribirlas en minúsculas.
    
- En XML se distinguen mayúsculas y minúsculas.
    
- Existen elementos HTML que no necesitan etiqueta de cierre, como `<br>`, `<img>` y `<hr>`.
    
- Algunos elementos HTML permiten omitir la etiqueta de cierre en determinadas circunstancias.
    

> [!IMPORTANT] Para el examen  
> Las etiquetas permiten identificar y delimitar las distintas partes de un documento.

---

## B. Elementos

Un **elemento** representa una estructura lógica completa dentro de un documento.

Generalmente está formado por:

**Etiqueta de apertura + contenido + etiqueta de cierre.**

**Ejemplo:**

```
<p>Hola, mundo</p>
```

Todo el conjunto representa un elemento HTML.

### Elementos anidados

Los elementos pueden contener otros elementos, formando una **estructura jerárquica**.

**Ejemplo:**

```
<ul>
    <li><p>Primer elemento</p></li>
    <li><p>Segundo elemento</p></li>
</ul>
```

- `<ul>`: lista no ordenada.
    
- `<li>`: elemento de la lista.
    
- `<p>`: párrafo.
    

### Características

- Los elementos permiten organizar el contenido.
    
- Pueden contener texto y otros elementos.
    
- Algunos tienen etiquetas de cierre opcionales.
    
- Existen elementos vacíos que no contienen información interna.
    

**Ejemplos de elementos vacíos en HTML:**

```
<br>
<hr>
<img src="imagen.jpg" alt="Descripción">
```

> [!NOTE] Diferencia importante  
> **Etiqueta:** marca utilizada para identificar una estructura.
> 
> **Elemento:** estructura completa que puede incluir etiquetas, atributos y contenido.

---

## C. Atributos

Los **atributos** proporcionan información adicional sobre los elementos.

Se escriben dentro de la **etiqueta de apertura**.

Generalmente siguen esta estructura:

`nombre="valor"`

**Ejemplo:**

```
<html lang="es">
```

- `html`: elemento.
    
- `lang`: atributo.
    
- `"es"`: valor del atributo.
    

### Características

- Se incluyen en la etiqueta de apertura.
    
- Un elemento puede tener varios atributos.
    
- Los atributos se separan mediante espacios.
    
- Su orden generalmente es indiferente.
    
- Los valores pueden escribirse entre comillas simples o dobles.
    
- En HTML existen atributos booleanos que pueden aparecer sin valor explícito.
    

**Ejemplo con varios atributos:**

```
<img src="foto.jpg" alt="Mi fotografía">
```

|Atributo|Función|
|---|---|
|`src`|Indica la ubicación de la imagen.|
|`alt`|Define un texto alternativo.|
|`lang`|Indica el idioma.|
|`charset`|Indica la codificación de caracteres.|

### Codificación UTF-8

```
<meta charset="utf-8">
```

UTF-8 es una codificación de caracteres que permite representar letras, números, símbolos y caracteres especiales de numerosos idiomas.

> [!IMPORTANT] Para el examen  
> Los atributos añaden información adicional a un elemento y normalmente se escriben en su etiqueta de apertura.

---

## D. Metadatos

Los **metadatos** son datos que proporcionan información sobre otros datos o sobre el propio documento.

En HTML se utilizan para describir características de una página web.

### ¿Qué información pueden proporcionar?

- Autor del documento.
    
- Descripción de la página.
    
- Codificación de caracteres.
    
- Otra información destinada a navegadores y aplicaciones.
    

### Ejemplos

**Autor del documento:**

```
<meta name="author" content="Alberto">
```

**Descripción de la página:**

```
<meta name="description" content="Apuntes de ASIR">
```

**Codificación de caracteres:**

```
<meta charset="UTF-8">
```

### Características

- Los elementos `<meta>` se colocan dentro de `<head>` en HTML.
    
- Proporcionan información sobre el documento.
    
- Generalmente no se muestran directamente en el contenido de la página.
    
- Algunos metadatos pueden ser utilizados por los motores de búsqueda.
    

### Relación con el SEO

El **SEO (Search Engine Optimization)** es el conjunto de técnicas destinadas a mejorar la visibilidad de una página en los buscadores.

Los metadatos pueden ayudar a describir el contenido de una página para los buscadores.

> [!IMPORTANT] Para el examen  
> Los metadatos proporcionan información sobre el propio documento, como el autor, la descripción o la codificación.

---

## Resumen general para el examen

|Concepto|Definición|Ejemplo|
|---|---|---|
|**Etiqueta**|Código que identifica o delimita una estructura.|`<p>`|
|**Elemento**|Estructura lógica completa.|`<p>Texto</p>`|
|**Atributo**|Información adicional de un elemento.|`lang="es"`|
|**Metadato**|Información sobre el documento.|`<meta charset="UTF-8">`|

> [!TIP] Truco para memorizar
> 
> - **Etiqueta:** identifica una parte.
>     
> - **Elemento:** representa la estructura completa.
>     
> - **Atributo:** añade información al elemento.
>     
> - **Metadato:** describe el documento.
>     

## Ejemplo completo

```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="author" content="Alberto">
    <title>Mis apuntes</title>
</head>
<body>
    <h1>Lenguajes de marcas</h1>
    <p>Estoy estudiando ASIR.</p>
</body>
</html>
```

En este ejemplo aparecen los cuatro conceptos:

1. **Etiquetas:** `<h1>`, `<p>`, `<head>`.
    
2. **Elementos:** `<h1>Lenguajes de marcas</h1>`.
    
3. **Atributos:** `lang="es"`, `charset="UTF-8"`.
    
4. **Metadatos:** información definida mediante `<meta>`.
    

**Conclusión:** estos cuatro conceptos constituyen la base para comprender la estructura de documentos HTML y XML.

# 3. Evolución de los lenguajes de marcas

Los lenguajes de marcas han evolucionado para facilitar la estructuración, presentación e intercambio de información.

Los principales son:

- **SGML (1986):** estándar para definir lenguajes de marcas.
    
- **HTML (1991):** lenguaje para estructurar páginas web.
    
- **XML (1998):** metalenguaje para representar e intercambiar datos.
    
- **XHTML (2000):** reformulación de HTML siguiendo las reglas de XML.
    

## A. SGML

**SGML (Standard Generalized Markup Language)** es un metalenguaje estandarizado en 1986 mediante la norma ISO 8879.

Un **metalenguaje** es un lenguaje que permite definir otros lenguajes.

### Características

- Es un estándar internacional.
    
- Es independiente del software y del sistema operativo.
    
- Permite crear lenguajes de marcas específicos.
    
- Describe la estructura lógica de los documentos.
    
- No determina directamente su presentación visual.
    
- Es potente y flexible, pero complejo.
    

### Principales componentes

**1. Declaración SGML**

Define las características generales de la sintaxis SGML utilizada.

**2. DTD (Document Type Definition)**

Establece las reglas y la estructura que debe cumplir un documento.

Ejemplo:

```
<!ELEMENT libro (titulo, autor)>
<!ELEMENT titulo (#PCDATA)>
<!ELEMENT autor (#PCDATA)>
```

Esta DTD establece que un libro debe contener un título y un autor.

**3. Instancia del documento**

Es el documento real que contiene la información estructurada según las reglas definidas.

### Otros conceptos importantes

**Parser:** programa que analiza un documento y comprueba que cumple las reglas sintácticas y, cuando corresponde, las de validación.

**Entidades:** mecanismos para representar caracteres, reutilizar contenido o referenciar recursos externos.

> [!IMPORTANT] Para el examen  
> SGML es un **metalenguaje** que permite definir lenguajes de marcas específicos. Utiliza DTD para establecer las reglas de los documentos.

---

## B. HTML

**HTML (HyperText Markup Language)** es un lenguaje de marcas utilizado para estructurar páginas web.

Fue desarrollado inicialmente por Tim Berners-Lee a principios de los años noventa y deriva históricamente de SGML.

### Características

- Utiliza etiquetas definidas por un estándar.
    
- Permite organizar títulos, párrafos, listas, imágenes y enlaces.
    
- Los navegadores interpretan sus documentos.
    
- Es relativamente sencillo de aprender.
    
- Se utiliza junto con CSS y JavaScript.
    

### Ejemplo HTML

```
<!DOCTYPE html>
<html lang="es">
<head>
    <title>Mi página</title>
</head>
<body>
    <h1>Lenguajes de marcas</h1>
    <p>Estoy estudiando ASIR.</p>
</body>
</html>
```

### Limitaciones históricas

- Dispone de un vocabulario estandarizado de etiquetas.
    
- No está diseñado principalmente para almacenar datos estructurados.
    
- Las primeras versiones mezclaban aspectos de estructura y presentación.
    
- Es menos flexible que SGML para definir vocabularios documentales personalizados.
    

> [!NOTE] Aclaración  
> HTML5 ha mejorado considerablemente la estructura semántica y las capacidades de HTML. Algunas limitaciones del temario se refieren a sus versiones antiguas.

> [!IMPORTANT] Para el examen  
> HTML se utiliza principalmente para **estructurar y presentar contenido en páginas web**.

---

## C. XML

**XML (eXtensible Markup Language)** es un metalenguaje extensible cuya primera recomendación oficial se publicó en 1998.

Es una simplificación de SGML diseñada para facilitar la representación y el intercambio de información estructurada.

### Características principales

1. Permite crear etiquetas y atributos personalizados.
    
2. Describe información estructurada.
    
3. Es independiente del software y de la plataforma.
    
4. Permite validar documentos mediante DTD o esquemas XML.
    
5. Separa los datos de su presentación visual.
    
6. Puede utilizarse para generar otros formatos mediante transformaciones.
    
7. Admite Unicode y diferentes codificaciones.
    
8. Es un estándar abierto y no requiere licencias.
    

### Ejemplo XML

```
<alumno>
    <nombre>Alberto</nombre>
    <curso>ASIR</curso>
    <nota>9</nota>
</alumno>
```

Las etiquetas describen el significado de cada dato.

### ¿Por qué es extensible?

Porque permite definir etiquetas adaptadas a las necesidades de cada aplicación.

Por ejemplo:

```
<producto>
    <nombre>Teclado</nombre>
    <precio>35</precio>
</producto>
```

### Transformación de documentos

XML puede procesarse mediante herramientas como XSLT para generar documentos HTML y otros formatos.

> [!IMPORTANT] Para el examen  
> XML es un **metalenguaje extensible** utilizado principalmente para almacenar, estructurar e intercambiar información.

---

## D. Comparativa: XML y HTML

|Característica|XML|HTML|
|---|---|---|
|Tipo|Metalenguaje|Lenguaje de marcas|
|Origen|Simplificación de SGML|Derivado de SGML|
|Finalidad|Estructurar e intercambiar datos|Estructurar páginas web|
|Etiquetas|Personalizables|Predefinidas|
|Presentación|No define presentación por defecto|Representación mediante navegadores|
|Sintaxis|Estricta|Más flexible|
|Mayúsculas|Distingue|Generalmente no distingue|
|Cierre|Obligatorio o autocierre|Algunos cierres opcionales|

### Ejemplo comparativo

**HTML:**

```
<h1>Alberto</h1>
<p>Estudiante de ASIR</p>
```

**XML:**

```
<persona>
    <nombre>Alberto</nombre>
    <estudios>ASIR</estudios>
</persona>
```

**Diferencia fundamental:**

- HTML identifica la estructura del contenido web.
    
- XML identifica la estructura y el significado de los datos.
    

---

## E. Comparativa: XML y SGML

|Característica|XML|SGML|
|---|---|---|
|Complejidad|Menor|Mayor|
|Relación|Subconjunto simplificado|Metalenguaje original|
|Sintaxis|Estricta|Más flexible|
|DTD|Opcional|Fundamental en su modelo tradicional|
|Uso|Muy extendido|Más especializado|
|Procesamiento|Más sencillo|Más complejo|

### ¿Por qué surgió XML?

SGML era un sistema potente, pero complejo de implementar.

XML se desarrolló para conservar sus principales ventajas y simplificar su utilización.

> [!TIP] Truco para memorizar  
> **SGML:** crea lenguajes de marcas.
> 
> **HTML:** estructura páginas web.
> 
> **XML:** estructura e intercambia datos.
> 
> **XHTML:** HTML con reglas sintácticas de XML.

---

## Resumen general para el examen

|Lenguaje|Año|Función principal|
|---|---|---|
|SGML|1986|Definir lenguajes de marcas|
|HTML|1991|Estructurar páginas web|
|XML|1998|Representar e intercambiar datos|
|XHTML|2000|Aplicar reglas XML al vocabulario HTML|

### Conceptos que debes memorizar

- **Metalenguaje:** lenguaje que permite definir otros lenguajes.
    
- **DTD:** establece la estructura y las reglas de un documento.
    
- **Parser:** programa que analiza la sintaxis y puede comprobar la validez del documento.
    
- **Entidad:** mecanismo para representar o reutilizar contenido.
    
- **SGML:** estándar general, potente y complejo.
    
- **HTML:** lenguaje de marcas para páginas web.
    
- **XML:** metalenguaje extensible, más sencillo que SGML.
    
- **XHTML:** reformulación de HTML basada en XML.
    

> [!IMPORTANT] Idea principal del tema  
> SGML dio origen a HTML y XML. HTML se especializó en documentos web, mientras que XML se diseñó para representar e intercambiar datos estructurados mediante etiquetas personalizadas.

# 4. Iniciación a XML

## A. Origen del XML

**XML (eXtensible Markup Language)** es un metalenguaje derivado de SGML, cuya primera recomendación oficial fue publicada por el W3C en 1998.

Surgió para facilitar el almacenamiento, la estructuración y el intercambio de información entre diferentes aplicaciones.

### Evolución histórica

|Año|Acontecimiento|
|---|---|
|1986|Normalización de SGML.|
|1991|Primeras versiones de HTML.|
|1994|Fundación del W3C.|
|1998|Publicación de XML 1.0.|
|2000|Publicación de XHTML 1.0.|
|2014|HTML5 se convierte en recomendación del W3C.|

**XHTML:** reformulación de HTML que utiliza las reglas sintácticas de XML.

**Web semántica:** iniciativa para facilitar que los sistemas informáticos interpreten el significado y las relaciones de la información.

> [!IMPORTANT] Para el examen  
> XML surgió como una simplificación de SGML para representar e intercambiar información estructurada mediante etiquetas personalizadas.

---

## B. Características del metalenguaje XML

XML es un **metalenguaje descriptivo o semántico** que permite crear vocabularios de etiquetas para estructurar información.

### Características principales

1. **Extensible:** permite crear etiquetas y atributos personalizados.
    
2. **Interoperable:** facilita el intercambio de información entre aplicaciones y sistemas.
    
3. **Texto:** los documentos suelen almacenarse en archivos `.xml`.
    
4. **Jerárquico:** organiza los elementos en forma de árbol.
    
5. **Estricto:** exige cumplir unas reglas sintácticas.
    
6. **Independiente de la presentación:** describe datos sin definir necesariamente cómo se muestran.
    
7. **Validable:** permite comprobar reglas mediante DTD o esquemas XML.
    

### Ejemplo

```
<alumno>
    <nombre>Alberto</nombre>
    <curso>ASIR</curso>
</alumno>
```

### Bien formado y válido

- **Bien formado:** cumple las reglas sintácticas de XML.
    
- **Válido:** está bien formado y cumple las reglas de una DTD o esquema.
    

> [!IMPORTANT] Diferencia  
> Un documento puede estar bien formado sin ser válido, pero para ser válido debe estar bien formado.

---

## C. Marcado del documento

El **marcado** consiste en utilizar etiquetas para identificar y estructurar el contenido.

### Etiquetas y elementos

```
<titulo>Aprender XML</titulo>
```

- `<titulo>`: etiqueta de apertura.
    
- `Aprender XML`: contenido.
    
- `</titulo>`: etiqueta de cierre.
    
- Todo el conjunto: elemento completo.
    

### Atributos

Los atributos añaden propiedades o información adicional a los elementos.

```
<libro id="1" idioma="es">
    <titulo>XML</titulo>
</libro>
```

- `id` e `idioma`: atributos.
    
- `"1"` y `"es"`: valores.
    

**Reglas de los atributos:**

- Se escriben en la etiqueta de apertura.
    
- Sus valores deben ir entre comillas.
    
- Pueden existir varios atributos.
    
- No se puede repetir el mismo atributo dentro de una etiqueta de apertura.
    
- Los nombres distinguen mayúsculas y minúsculas.
    

### Elementos vacíos

Son elementos que no contienen información interna.

```
<salto/>
```

También pueden escribirse:

```
<salto></salto>
```

### Reglas para nombres de elementos

- No pueden comenzar por números.
    
- No pueden contener espacios.
    
- Distinguen mayúsculas y minúsculas.
    
- Pueden contener letras, números y determinados símbolos como `_`, `-` y `.`.
    
- No deben comenzar por la secuencia `xml`, en ninguna combinación de mayúsculas y minúsculas.
    

### Anidamiento

Los elementos deben estar correctamente anidados.

**Correcto:**

```
<libro>
    <titulo>XML</titulo>
</libro>
```

**Incorrecto:**

```
<libro>
    <titulo>XML</libro>
</titulo>
```

### Caracteres especiales

|Carácter|Referencia XML|
|---|---|
|`<`|`&lt;`|
|`>`|`&gt;`|
|`&`|`&amp;`|
|`"`|`&quot;`|
|`'`|`&apos;`|

### Comentarios

Los comentarios sirven para documentar el código.

```
<!-- Datos del alumno -->
<alumno>
    <nombre>Alberto</nombre>
</alumno>
```

> [!IMPORTANT] Para el examen  
> XML exige etiquetas correctamente cerradas, anidamiento correcto, atributos entre comillas y respeto de mayúsculas y minúsculas.

---

## D. Partes de un documento XML

Un documento XML se divide principalmente en:

1. **Prólogo.**
    
2. **Cuerpo del documento.**
    

### 1. Prólogo

Puede contener la declaración XML, instrucciones de procesamiento, comentarios y DOCTYPE.

**Declaración XML:**

```
<?xml version="1.0" encoding="UTF-8"?>
```

|Componente|Función|
|---|---|
|`version`|Versión del estándar XML.|
|`encoding`|Codificación de caracteres.|
|`standalone`|Indica la dependencia de declaraciones externas relevantes.|

**Ejemplo:**

```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
```

### DOCTYPE

Identifica el tipo de documento y puede incluir o referenciar una DTD.

```
<!DOCTYPE libro SYSTEM "libro.dtd">
```

**DTD (Document Type Definition):** establece reglas para la estructura de un documento.

### 2. Cuerpo del documento

Contiene la información organizada mediante elementos.

```
<libro>
    <titulo>Aprender XML</titulo>
    <autor>Alberto</autor>
    <precio>25</precio>
</libro>
```

**Reglas de la estructura:**

- Debe existir un único elemento raíz.
    
- Los elementos forman una estructura jerárquica.
    
- Los elementos deben estar correctamente anidados.
    
- El contenido debe encontrarse dentro del elemento raíz, salvo las construcciones permitidas en el prólogo y epílogo.
    

> [!TIP] Truco  
> **Prólogo:** información inicial y declaraciones.
> 
> **Cuerpo:** estructura y contenido del documento.

---

## E. Documento XML bien formado

Un documento XML está **bien formado** cuando cumple las reglas sintácticas establecidas por XML.

### Reglas fundamentales

1. Tiene un único elemento raíz.
    
2. Todos los elementos están correctamente cerrados.
    
3. Los elementos están correctamente anidados.
    
4. Se distinguen mayúsculas y minúsculas.
    
5. Los atributos tienen valores entre comillas.
    
6. Los nombres respetan las reglas de XML.
    
7. Los caracteres especiales se utilizan correctamente.
    
8. La declaración XML, si se incluye, debe estar correctamente escrita y situada al principio.
    

### Ejemplo correcto

```
<?xml version="1.0" encoding="UTF-8"?>
<alumnos>
    <alumno id="1">
        <nombre>Alberto</nombre>
        <curso>ASIR</curso>
    </alumno>
</alumnos>
```

### Ejemplo incorrecto

```
<alumnos>
    <alumno>
        <nombre>Alberto</Nombre>
    </alumno>
</alumnos>
```

**Error:** las etiquetas `<nombre>` y `</Nombre>` no coinciden.

### Diferencia entre bien formado y válido

|Documento bien formado|Documento válido|
|---|---|
|Cumple la sintaxis XML.|Cumple la sintaxis y las reglas de validación.|
|No necesita DTD.|Necesita DTD o esquema.|
|Tiene una estructura sintácticamente correcta.|Respeta además la estructura definida por el esquema.|

> [!IMPORTANT] Para el examen  
> **Bien formado = sintaxis correcta.**
> 
> **Válido = sintaxis correcta + cumplimiento de DTD o esquema.**

---

## Resumen general del apartado 4

|Concepto|Definición|
|---|---|
|XML|Metalenguaje extensible para representar datos estructurados.|
|W3C|Organismo que desarrolla estándares web.|
|XHTML|Reformulación de HTML basada en XML.|
|Etiqueta|Marca que identifica o delimita una estructura.|
|Elemento|Estructura completa que puede incluir etiquetas, atributos y contenido.|
|Atributo|Información adicional de un elemento.|
|Prólogo|Parte inicial con declaraciones.|
|DOCTYPE|Declaración del tipo de documento.|
|DTD|Reglas que definen la estructura permitida.|
|Elemento raíz|Elemento principal que contiene los demás elementos.|
|Parser|Programa que analiza la estructura y sintaxis de un documento.|
|Bien formado|Documento que cumple la sintaxis XML.|
|Válido|Documento que además cumple una DTD o esquema.|

### Lo más importante para memorizar

> [!IMPORTANT] Claves del examen
> 
> - XML apareció como recomendación del W3C en **1998**.
>     
> - Es un **metalenguaje extensible y descriptivo**.
>     
> - Permite crear etiquetas personalizadas.
>     
> - Organiza la información jerárquicamente.
>     
> - Todo documento XML debe tener **un único elemento raíz**.
>     
> - Las etiquetas deben cerrarse y anidarse correctamente.
>     
> - XML distingue mayúsculas y minúsculas.
>     
> - Los atributos deben llevar sus valores entre comillas.
>     
> - **Bien formado** significa sintaxis correcta.
>     
> - **Válido** significa cumplir además las reglas de una DTD o esquema.

# 5. Espacios de nombres en XML

## ¿Qué son los espacios de nombres?

Los **espacios de nombres (namespaces)** son un mecanismo de XML que permite diferenciar elementos y atributos de distintos vocabularios que utilizan el mismo nombre.

Su objetivo principal es **evitar conflictos y ambigüedades** cuando se combinan documentos o vocabularios XML.

### Ejemplo del problema

```xml
<capital>
    <pais>Francia</pais>
    <nombre>París</nombre>
</capital>
```

```xml
<capital>
    <bonos>
        <cantidad>10000</cantidad>
    </bonos>
</capital>
```

Ambos elementos se llaman `<capital>`, pero tienen significados distintos:

- Capital geográfica.
    
- Capital económico.
    

**Solución:** asignar un espacio de nombres diferente a cada vocabulario.

---

## Declaración de espacios de nombres

Los espacios de nombres se declaran utilizando `xmlns`.

**Sintaxis:**

```xml
xmlns:prefijo="URI"
```

|Componente|Función|
|---|---|
|`xmlns`|Declara un espacio de nombres.|
|`prefijo`|Alias utilizado en las etiquetas.|
|`URI`|Identificador del espacio de nombres.|

### Ejemplo

```xml
xmlns:capital="http://localhost/UD1/capital"
```

El prefijo `capital` queda asociado a la URI indicada.

### Uso del prefijo

```xml
<capital:capital>
    <pais>Francia</pais>
    <nombre>París</nombre>
</capital:capital>
```

En `<capital:capital>`:

- Primer `capital`: prefijo.
    
- `:`: separador.
    
- Segundo `capital`: nombre local del elemento.
    

> [!IMPORTANT] Para el examen  
> El prefijo es un alias. La URI es la que identifica el espacio de nombres.

---

## Ejemplo completo

```xml
<?xml version="1.0" encoding="UTF-8"?>

<datos
    xmlns:capital="http://localhost/UD1/capital"
    xmlns:contab="http://localhost/UD1/contab">

    <capital:capital>
        <pais>Francia</pais>
        <nombre>París</nombre>
    </capital:capital>

    <contab:capital>
        <bonos>
            <cantidad>10000</cantidad>
        </bonos>
        <letras>
            <precio>1000</precio>
        </letras>
    </contab:capital>

</datos>
```

**Explicación:**

- `xmlns:capital`: declara el espacio de nombres geográfico.
    
- `xmlns:contab`: declara el espacio de nombres financiero.
    
- `<capital:capital>`: pertenece al vocabulario geográfico.
    
- `<contab:capital>`: pertenece al vocabulario financiero.
    

Así se evita la confusión entre elementos que tienen el mismo nombre.

---

## URI y URL

### URI (Uniform Resource Identifier)

Es una cadena de caracteres que permite identificar un recurso de forma uniforme.

En XML se utiliza para identificar espacios de nombres.

### URL (Uniform Resource Locator)

Es un tipo de URI que identifica un recurso indicando su localización o forma de acceso.

### Diferencia

|URI|URL|
|---|---|
|Identifica un recurso.|Identifica un recurso mediante su localización o acceso.|
|No necesita indicar dónde acceder al recurso.|Proporciona información para localizarlo o acceder a él.|
|Se utiliza para identificar namespaces.|Se utiliza habitualmente en direcciones web.|

> [!NOTE]  
> Las URI de los espacios de nombres XML no necesitan corresponder a páginas web existentes. Su función es identificar el vocabulario.

---

## Relación con DTD y Schema

Los espacios de nombres permiten diferenciar vocabularios XML.

Las DTD y los esquemas permiten definir reglas sobre la estructura y el contenido de los documentos.

- **Namespace:** identifica el vocabulario.
    
- **DTD / Schema:** define reglas de validación.
    

---

## Resumen para el examen

|Concepto|Definición|
|---|---|
|Espacio de nombres|Permite diferenciar elementos o atributos con el mismo nombre.|
|`xmlns`|Sintaxis para declarar un namespace.|
|Prefijo|Alias asociado a un espacio de nombres.|
|URI|Identificador uniforme de recursos.|
|URL|Localizador uniforme de recursos.|
|DTD / Schema|Define reglas para validar documentos XML.|

> [!IMPORTANT] Lo más importante
> 
> 1. Los espacios de nombres evitan conflictos entre etiquetas con el mismo nombre.
>     
> 2. Se declaran mediante `xmlns`.
>     
> 3. Utilizan prefijos asociados a URI.
>     
> 4. La URI identifica el espacio de nombres.
>     
> 5. Los prefijos permiten distinguir elementos de distintos vocabularios.
>     

**Truco para memorizar:**

`xmlns` = declaración del espacio de nombres.

`prefijo` = alias.

`URI` = identificador.

`prefijo:elemento` = elemento perteneciente al espacio de nombres.