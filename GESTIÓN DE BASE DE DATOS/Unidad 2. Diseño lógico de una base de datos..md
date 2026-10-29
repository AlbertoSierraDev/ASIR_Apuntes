# 1. Diseño lógico de una base de datos. Modelado

### ¿Qué es el diseño de una base de datos?

El **diseño de una base de datos** es el proceso de analizar, organizar y estructurar la información que se desea almacenar, definiendo los elementos que la componen y las relaciones existentes entre ellos.

Antes de crear una base de datos es necesario realizar un análisis previo para determinar:

- **Qué datos necesitamos almacenar.**
    
- **Cómo se agrupan esos datos.**
    
- **Qué relaciones existen entre ellos.**
    
- **Qué requisitos debe cumplir la base de datos.**
    

Un buen diseño permite evitar duplicidades innecesarias, reducir errores, mantener la integridad de los datos y facilitar su consulta y mantenimiento.

### ¿Qué es el modelado de datos?

El **modelado de datos** es el proceso de representar de forma organizada la información que almacenará una base de datos, identificando sus elementos, características y relaciones.

Su objetivo es crear una representación comprensible de los datos antes de implementarlos en un sistema gestor de bases de datos (SGBD).

### Modelado semántico

El **modelado semántico** consiste en representar los datos según su significado y las relaciones que mantienen entre sí, sin depender de cómo se almacenarán físicamente.

También se conoce como **modelado conceptual**.

Sus principales características son:

- Es independiente del SGBD utilizado.
    
- Permite identificar entidades, atributos y relaciones.
    
- Facilita la comprensión del diseño.
    
- Permite compartir el diseño con otras personas.
    
- Facilita futuras modificaciones de la implementación.
    

**Ejemplo:**

En una biblioteca identificamos las entidades LIBRO, AUTOR y USUARIO.

Podemos establecer que:

- Un autor escribe libros.
    
- Un usuario solicita libros en préstamo.
    
- Un libro puede tener varios autores.
    

Estas relaciones pueden representarse sin necesidad de utilizar todavía MySQL, PostgreSQL u otro SGBD.

### Ventajas del modelado semántico

**1. Independencia tecnológica:** el modelo conceptual no depende del SGBD elegido.

**2. Facilidad de comprensión:** permite visualizar cómo se organiza la información.

**3. Trabajo en equipo:** facilita que diferentes personas comprendan y revisen el diseño.

**4. Mantenimiento:** permite modificar la implementación sin tener que redefinir necesariamente el significado de los datos y sus relaciones.

---

## 1.1. Recopilación de datos y definición de entidades

### Recopilación de datos

La **recopilación de datos** es la primera fase del diseño de una base de datos.

Consiste en reunir toda la información que necesitamos almacenar y analizarla para identificar los conceptos principales.

Inicialmente, los datos pueden encontrarse desorganizados. Por ello, debemos clasificarlos y agruparlos según los elementos del mundo real que representan.

### ¿Qué es una entidad?

Una **entidad** es un objeto, persona, lugar, acontecimiento o concepto del mundo real sobre el que necesitamos almacenar información.

**Ejemplos de entidades:**

- ALUMNO
    
- PROFESOR
    
- PELÍCULA
    
- CLIENTE
    
- PRODUCTO
    
- PEDIDO
    

Las entidades representan los elementos principales de nuestra base de datos.

### ¿Qué es un atributo?

Un **atributo** es una característica o propiedad que describe una entidad.

Cada entidad puede tener varios atributos.

**Ejemplo:**

Entidad: ALUMNO

|Atributo|Valor|
|---|---|
|ID|1|
|Nombre|Alberto|
|Edad|24|
|Curso|ASIR|

- **Entidad:** ALUMNO.
    
- **Atributos:** ID, nombre, edad y curso.
    
- **Valores:** 1, Alberto, 24 y ASIR.
    

Una **instancia de una entidad** es un elemento concreto que pertenece a esa entidad.

Por ejemplo, Alberto es una instancia de ALUMNO.

### Ejemplo de recopilación y clasificación de datos

Queremos diseñar una base de datos para gestionar una colección de películas.

Necesitamos almacenar:

- Nombre de las películas.
    
- Género.
    
- Año de estreno.
    
- Formato.
    
- Nombre de los directores.
    
- Nacionalidad de los directores.
    
- Nombre de los actores.
    
- Nacionalidad de los actores.
    
- Personajes interpretados.
    

Después de analizar la información identificamos tres entidades principales.

**Entidad PELÍCULA**

|Atributo|Descripción|
|---|---|
|Nombre|Título de la película|
|Género|Categoría cinematográfica|
|Año|Año de estreno|
|Formato|Formato de almacenamiento|

**Entidad DIRECTOR**

|Atributo|Descripción|
|---|---|
|Nombre|Nombre del director|
|Nacionalidad|País de origen o nacionalidad|

**Entidad ACTOR**

|Atributo|Descripción|
|---|---|
|Nombre|Nombre del actor|
|Nacionalidad|Nacionalidad del actor|

**Importante:** el personaje interpretado por un actor puede modelarse como un atributo de la relación entre ACTOR y PELÍCULA, ya que un mismo actor puede interpretar diferentes personajes en distintas películas.

### Diferencia entre entidad y atributo

|Entidad|Atributo|
|---|---|
|Representa un elemento o concepto.|Describe una característica de una entidad.|
|Puede tener múltiples atributos.|Tiene valores concretos.|
|Ejemplo: PELÍCULA.|Ejemplo: título, género, año.|
|Ejemplo: CLIENTE.|Ejemplo: nombre, correo electrónico.|

**Concepto clave:** una entidad representa aquello sobre lo que queremos almacenar información, mientras que sus atributos describen sus características.

---

## 1.2. Empezando con las relaciones

### ¿Qué es una relación?

Una **relación** es una asociación existente entre dos o más entidades de una base de datos.

Las relaciones permiten representar cómo se conectan los diferentes elementos de la información.

**Ejemplo:**

Tenemos las entidades:

- DIRECTOR
    
- PELÍCULA
    
- ACTOR
    

Podemos identificar las siguientes relaciones:

**DIRECTOR — dirige — PELÍCULA**

**ACTOR — participa en — PELÍCULA**

Gracias a estas relaciones podemos responder preguntas como:

- ¿Quién dirige una película?
    
- ¿Qué películas ha dirigido un director?
    
- ¿Qué actores participan en una película?
    
- ¿En qué películas ha participado un actor?
    

### Importancia de las relaciones

Las relaciones permiten:

- Conectar la información de diferentes entidades.
    
- Representar asociaciones del mundo real.
    
- Consultar información relacionada.
    
- Evitar duplicidades innecesarias.
    
- Mantener la coherencia de los datos.
    

### Cardinalidad de las relaciones

La **cardinalidad** indica cuántas instancias de una entidad pueden relacionarse con instancias de otra entidad.

Los tres tipos habituales son:

|Cardinalidad|Nombre|Ejemplo|
|---|---|---|
|1:1|Uno a uno|Persona — DNI|
|1|Uno a muchos|Departamento — Empleado|
|N|Muchos a muchos|Actor — Película|

**Relación 1:1 (uno a uno)**

Una instancia de una entidad se relaciona, como máximo, con una instancia de la otra entidad, y viceversa.

Ejemplo: una persona y su DNI, suponiendo que cada persona tenga uno.

**Relación 1 (uno a muchos)**

Una instancia de una entidad puede relacionarse con varias instancias de otra entidad.

Ejemplo:

- Un departamento tiene varios empleados.
    
- Cada empleado pertenece a un departamento.
    

**Relación N (muchos a muchos)**

Varias instancias de una entidad pueden relacionarse con varias instancias de otra.

Ejemplo:

- Un actor puede participar en muchas películas.
    
- Una película puede tener muchos actores.
    

**Importante:** la cardinalidad depende de las reglas del sistema que estamos diseñando.

### Diferencia entre atributo y relación

Un **atributo** describe una característica de una entidad.

Una **relación** representa una asociación entre entidades.

**Ejemplo:**

Entidad CLIENTE:

- Nombre → Atributo.
    
- Correo electrónico → Atributo.
    

Entidad PEDIDO:

- Fecha → Atributo.
    
- Estado → Atributo.
    

Asociación:

**CLIENTE — realiza — PEDIDO**

Esta asociación es una relación porque conecta dos entidades.

---

## Proceso de modelado de una base de datos

El proceso explicado en el temario sigue estas fases:

### 1. Recopilación de datos

Reunir toda la información que necesita almacenar el sistema.

### 2. Análisis y clasificación

Organizar los datos e identificar las entidades y sus atributos.

### 3. Modelado semántico o conceptual

Representar las entidades y sus relaciones sin depender de una implementación concreta.

Una herramienta habitual es el **modelo entidad-relación (ER)**.

### 4. Modelado estructural

Transformar el modelo conceptual en una estructura adecuada al modelo de datos elegido.

Por ejemplo:

- Modelo relacional.
    
- Modelo orientado a objetos.
    
- Modelo documental.
    

### Diferencia entre modelado semántico y estructural

|Modelado semántico|Modelado estructural|
|---|---|
|Representa el significado de los datos.|Define cómo se organizan los datos.|
|Identifica entidades y relaciones.|Define estructuras concretas.|
|Es independiente del SGBD.|Se adapta al modelo de datos elegido.|
|Utiliza modelos como entidad-relación.|Puede utilizar tablas, objetos o documentos.|

**Ejemplo:**

**Modelo semántico:** un alumno cursa varias asignaturas.

**Modelo estructural relacional:** se diseñan las tablas ALUMNO, ASIGNATURA y, cuando corresponde, una tabla intermedia MATRÍCULA para representar esa relación.

---

## Conceptos clave para el examen

|Concepto|Definición|
|---|---|
|Diseño de bases de datos|Proceso de analizar y estructurar la información que se almacenará.|
|Modelado de datos|Representación organizada de los datos y sus relaciones.|
|Modelado semántico|Representación conceptual independiente del SGBD.|
|Entidad|Elemento o concepto sobre el que almacenamos información.|
|Atributo|Característica que describe una entidad.|
|Instancia|Elemento concreto perteneciente a una entidad.|
|Relación|Asociación entre dos o más entidades.|
|Cardinalidad|Cantidad de instancias que pueden asociarse entre entidades.|
|Modelo entidad-relación|Modelo conceptual utilizado para representar entidades, atributos y relaciones.|
|Modelado estructural|Adaptación del modelo conceptual a una estructura de datos determinada.|

### Ideas fundamentales

1. **Antes de crear una base de datos debemos analizar qué información necesitamos almacenar.**
    
2. **Las entidades representan elementos del mundo real.**
    
3. **Los atributos describen las características de las entidades.**
    
4. **Las relaciones conectan diferentes entidades.**
    
5. **La cardinalidad indica cuántas instancias pueden relacionarse.**
    
6. **El modelado semántico es independiente del SGBD.**
    
7. **El modelado estructural define cómo se organizarán los datos según el modelo elegido.**
    
8. **El modelo entidad-relación es una herramienta fundamental para diseñar bases de datos.**

# 2. Modelo entidad-relación: entidades, atributos y claves

## ¿Qué es el modelo entidad-relación (ER)?

El **modelo entidad-relación (ER)** es un modelo conceptual que permite representar gráficamente los datos que queremos almacenar en una base de datos y las relaciones existentes entre ellos.

Se utiliza durante la fase de diseño, antes de implementar la base de datos en un SGBD como MySQL.

Está formado principalmente por tres elementos:

- **Entidades:** representan objetos o conceptos del mundo real.
    
- **Atributos:** describen las características de las entidades.
    
- **Relaciones:** representan las asociaciones entre entidades.
    

**Ejemplo:**

En una base de datos de un instituto identificamos:

- Entidades: ALUMNO, PROFESOR y ASIGNATURA.
    
- Atributos de ALUMNO: ID, nombre y apellidos.
    
- Relaciones: un ALUMNO cursa una ASIGNATURA y un PROFESOR imparte una ASIGNATURA.
    

El modelo ER es independiente del SGBD utilizado.

---

## 2.1. Entidades

### Definición de entidad

Una **entidad** es un objeto, persona, lugar, acontecimiento o concepto del mundo real sobre el que necesitamos almacenar información.

Las entidades agrupan elementos que comparten una serie de características comunes y que pueden diferenciarse de otros elementos.

**Ejemplos:**

- ALUMNO
    
- PROFESOR
    
- PELÍCULA
    
- PRODUCTO
    
- CLIENTE
    
- VEHÍCULO
    

### Entidad e instancia

Es importante distinguir entre una entidad y una instancia.

- **Entidad:** representa un conjunto o categoría de elementos con características comunes.
    
- **Instancia:** es un elemento concreto perteneciente a una entidad.
    

**Ejemplo:**

Entidad: COCHE.

|Matrícula|Marca|Modelo|
|---|---|---|
|1234ABC|Seat|León|
|5678DEF|Toyota|Corolla|
|9012GHI|Volkswagen|Golf|

- COCHE es la entidad.
    
- Cada fila representa una instancia.
    
- Matrícula, marca y modelo son atributos.
    

### Representación gráfica de las entidades

En el modelo entidad-relación, las entidades se representan mediante **rectángulos** que contienen el nombre de la entidad.

Ejemplo:

```
┌──────────────┐
│   PELÍCULA   │
└──────────────┘

┌──────────────┐
│   DIRECTOR   │
└──────────────┘
```

**Para el examen:** las entidades se representan mediante rectángulos.

---

## 2.2. Atributos

### Definición de atributo

Un **atributo** es una propiedad o característica que describe una entidad.

Cada entidad puede tener varios atributos que permiten almacenar información sobre sus instancias.

**Ejemplo:**

Entidad: PELÍCULA.

Atributos:

- Nombre.
    
- Género.
    
- Año.
    
- Formato.
    

### Diferencia entre atributo y valor

Un atributo representa una característica general, mientras que un valor es la información concreta que toma ese atributo para una instancia.

**Ejemplo:**

|Atributo|Valor|
|---|---|
|Nombre|Interstellar|
|Género|Ciencia ficción|
|Año|2014|
|Formato|Digital|

- **Nombre:** atributo.
    
- **Interstellar:** valor.
    
- **Año:** atributo.
    
- **2014:** valor.
    

**Importante:** cuando diseñamos una entidad definimos sus atributos, no los valores concretos que almacenaremos posteriormente.

### Representación gráfica de los atributos

Los atributos pueden representarse de dos formas, según la notación utilizada.

**1. Dentro del rectángulo de la entidad**

```
┌────────────────┐
│    PELÍCULA    │
├────────────────┤
│ Nombre         │
│ Género         │
│ Año            │
│ Formato        │
└────────────────┘
```

**2. Mediante elipses**

En la notación clásica de Chen, cada atributo se representa mediante una **elipse conectada directamente a la entidad**.

Por ejemplo, la entidad PELÍCULA tendría cuatro elipses conectadas, correspondientes a nombre, género, año y formato.

**Para el examen:**

- Entidad → Rectángulo.
    
- Atributo → Elipse.
    
- En representaciones compactas, los atributos pueden aparecer dentro del rectángulo.
    

---

## 2.3. Claves

### ¿Qué es una clave?

Una **clave** es un atributo o conjunto de atributos que permite identificar de forma única cada instancia de una entidad.

Su función principal es diferenciar los elementos de una misma entidad, incluso cuando comparten otros atributos.

### Ejemplo de clave

Entidad: ALUMNO.

|ID_Alumno|Nombre|Edad|
|---|---|---|
|1|Alberto|24|
|2|Alberto|24|
|3|María|22|

En este ejemplo:

- Nombre no sirve como clave porque puede repetirse.
    
- Edad tampoco sirve porque puede repetirse.
    
- **ID_Alumno sí sirve como clave porque identifica de forma única cada alumno.**
    

### Características de una clave identificadora

Una clave debe cumplir las siguientes condiciones:

1. **Unicidad:** no puede identificar a dos instancias diferentes con el mismo valor o combinación de valores.
    
2. **Identificación:** debe permitir distinguir inequívocamente cada instancia.
    
3. **Minimalidad:** en una clave candidata no deben existir atributos innecesarios.
    

Además, es recomendable elegir identificadores estables, que no cambien frecuentemente.

Cuando una clave se selecciona como **clave primaria**, sus valores no pueden ser nulos.

### Tipos de claves

#### 1. Clave natural

Es una clave formada por uno o varios atributos que ya tienen significado en el mundo real.

**Ejemplos:**

- DNI de una persona, dentro de un ámbito donde sea único.
    
- Matrícula de un vehículo, dentro de un ámbito determinado.
    

#### 2. Clave artificial o sustituta

Es un identificador creado específicamente para distinguir las instancias de una entidad.

Se utiliza cuando no existe una clave natural adecuada o cuando resulta más conveniente disponer de un identificador independiente de los datos.

**Ejemplos:**

- ID_Alumno.
    
- ID_Cliente.
    
- ID_Producto.
    
- ID_Pelicula.
    

**Ejemplo:**

|ID_Pelicula|Nombre|Año|
|---|---|---|
|1|King Kong|1933|
|2|King Kong|2005|
|3|King Kong|2005|

Aunque dos películas tengan el mismo nombre y año, sus identificadores son diferentes.

#### 3. Clave compuesta

Una **clave compuesta** está formada por dos o más atributos que, conjuntamente, permiten identificar de forma única una instancia.

**Ejemplo:**

Entidad: MATRÍCULA.

|ID_Alumno|ID_Asignatura|Nota|
|---|---|---|
|1|10|8|
|1|20|7|
|2|10|9|
|2|20|6|

En este ejemplo:

- ID_Alumno no es único porque se repite.
    
- ID_Asignatura tampoco es único.
    
- La combinación **ID_Alumno + ID_Asignatura** es única.
    

Por tanto, podemos utilizar ambos atributos como clave compuesta, siempre que un alumno solo pueda tener una matrícula por asignatura.

Si el sistema permite matricularse varias veces en una misma asignatura, necesitaríamos incluir otro atributo identificador, como el curso académico, o utilizar un ID de matrícula.

### Diferencia entre clave natural, artificial y compuesta

|Tipo|Definición|Ejemplo|
|---|---|---|
|Natural|Utiliza datos con significado en el mundo real.|DNI|
|Artificial|Identificador creado para distinguir instancias.|ID_Alumno|
|Compuesta|Formada por varios atributos.|ID_Alumno + ID_Asignatura|

**Importante:** una clave compuesta también puede ser natural o estar formada por identificadores artificiales.

### ¿Cómo se representan las claves en el modelo ER?

En el temario aparecen dos formas.

**1. Mediante una almohadilla (#)**

En representaciones compactas, se coloca `#` delante del atributo identificador.

```
┌────────────────┐
│    PELÍCULA    │
├────────────────┤
│ #Código        │
│ Nombre         │
│ Género         │
│ Año            │
│ Formato        │
└────────────────┘
```

**2. Mediante el subrayado**

En la notación clásica de Chen, el nombre del atributo clave aparece subrayado dentro de su elipse.

Por ejemplo, en PELÍCULA se subrayaría el atributo Código.

---

## Diferencia entre entidad, atributo, instancia, valor y clave

|Concepto|Definición|Ejemplo|
|---|---|---|
|Entidad|Categoría de elementos con características comunes.|ALUMNO|
|Atributo|Característica de una entidad.|Nombre|
|Instancia|Elemento concreto de una entidad.|Un alumno determinado|
|Valor|Dato concreto de un atributo.|Alberto|
|Clave|Atributo o conjunto de atributos que identifica una instancia.|ID_Alumno|

---

## Conceptos clave para el examen

1. **El modelo entidad-relación permite representar conceptualmente los datos de una base de datos.**
    
2. **Las entidades se representan mediante rectángulos.**
    
3. **Los atributos describen las características de las entidades.**
    
4. **En la notación clásica, los atributos se representan mediante elipses.**
    
5. **Una instancia es un elemento concreto de una entidad.**
    
6. **Los atributos no son valores concretos.**
    
7. **Las claves permiten identificar de forma única cada instancia.**
    
8. **Una clave puede estar formada por uno o varios atributos.**
    
9. **Las claves naturales utilizan datos con significado propio.**
    
10. **Las claves artificiales son identificadores creados específicamente.**
    
11. **Las claves compuestas utilizan varios atributos conjuntamente.**
    
12. **En el modelo ER clásico, los atributos clave se representan subrayados.**
    
13. **En la representación compacta del temario, las claves se identifican mediante** `**#**`**.**
    



# 3. Modelo entidad-relación: relaciones y grados

## ¿Qué es una relación?

Una **relación** es una asociación existente entre dos o más entidades de una base de datos.

Las relaciones permiten conectar entidades y representar cómo interactúan los diferentes elementos del mundo real.

**Ejemplo:**

Tenemos dos entidades:

- PELÍCULA.
    
- DIRECTOR.
    

Entre ellas existe la relación **DIRIGE**.

`DIRECTOR — DIRIGE — PELÍCULA`

Esta relación permite conocer:

- Qué director ha dirigido una película.
    
- Qué películas ha dirigido un director.
    

Las relaciones son fundamentales porque permiten representar las asociaciones entre los datos.

---

## 3.1. Representación gráfica de las relaciones en el modelo ER

En el modelo entidad-relación clásico, las relaciones se representan mediante **rombos** conectados a las entidades mediante líneas.

Dentro del rombo se escribe el nombre de la relación.

### Elementos gráficos del modelo ER

|Elemento|Representación|
|---|---|
|Entidad|Rectángulo|
|Atributo|Elipse|
|Relación|Rombo|
|Clave|Atributo subrayado|
|Conexión|Línea|

### Ejemplo

Tenemos las entidades PELÍCULA y DIRECTOR.

Entre ellas existe la relación RODAJE.

`PELÍCULA — RODAJE — DIRECTOR`

En un diagrama ER clásico:

- PELÍCULA se representa mediante un rectángulo.
    
- DIRECTOR se representa mediante otro rectángulo.
    
- RODAJE se representa mediante un rombo.
    
- Las líneas conectan el rombo con ambas entidades.
    

### ¿Cómo se nombran las relaciones?

Normalmente se utilizan **verbos o expresiones verbales** que describen la asociación entre entidades.

Ejemplos:

|Entidad 1|Relación|Entidad 2|
|---|---|---|
|ALUMNO|CURSA|ASIGNATURA|
|PROFESOR|IMPARTE|ASIGNATURA|
|CLIENTE|REALIZA|PEDIDO|
|DIRECTOR|DIRIGE|PELÍCULA|
|EMPLEADO|TRABAJA EN|DEPARTAMENTO|

**Importante:** el nombre de una relación debe describir claramente la asociación existente entre las entidades.

---

## 3.2. Grado de una relación

El **grado de una relación** es el número de entidades que participan en ella.

Según el número de entidades participantes, podemos distinguir:

- **Grado 1:** relación unaria.
    
- **Grado 2:** relación binaria.
    
- **Grado 3:** relación ternaria.
    

### 1. Relación unaria (grado 1)

Una **relación unaria** es aquella en la que una entidad se relaciona consigo misma.

También se denomina **relación recursiva o reflexiva**.

**Ejemplo:**

En una empresa, un empleado puede ser jefe de otros empleados.

Entidad: EMPLEADO.

Relación: ES JEFE DE.

`EMPLEADO — ES JEFE DE — EMPLEADO`

Aunque aparecen dos participaciones de EMPLEADO, solo interviene un tipo de entidad.

Por tanto, es una relación de **grado 1**.

En esta relación existen dos roles:

- **Jefe:** empleado que dirige a otros.
    
- **Subordinado:** empleado que depende de un jefe.
    

**Importante:** no es necesario crear una entidad JEFE si los jefes también son empleados y pueden representarse mediante la entidad EMPLEADO.

### 2. Relación binaria (grado 2)

Una **relación binaria** es aquella en la que participan dos entidades.

Es uno de los tipos de relaciones más habituales.

**Ejemplo:**

`PROFESOR — IMPARTE — ASIGNATURA`

Participan dos entidades:

1. PROFESOR.
    
2. ASIGNATURA.
    

Por tanto, es una relación de **grado 2**.

Otros ejemplos:

- CLIENTE — REALIZA — PEDIDO.
    
- ALUMNO — CURSA — ASIGNATURA.
    
- DIRECTOR — DIRIGE — PELÍCULA.
    

### 3. Relación ternaria (grado 3)

Una **relación ternaria** es aquella en la que participan tres entidades simultáneamente.

Se utiliza cuando necesitamos representar una asociación conjunta entre tres entidades.

**Ejemplo:**

Queremos almacenar información sobre:

- ACTOR.
    
- PELÍCULA.
    
- PERSONAJE.
    

Necesitamos saber qué actor interpreta a qué personaje en cada película.

Creamos una relación llamada **INTERPRETA EN**.

`ACTOR — INTERPRETA EN — PELÍCULA — PERSONAJE`

Las tres entidades participan en una misma relación.

Ejemplo de datos:

|Actor|Película|Personaje|
|---|---|---|
|Christian Bale|Batman Begins|Bruce Wayne|
|Christian Bale|The Dark Knight|Bruce Wayne|
|Heath Ledger|The Dark Knight|Joker|

La relación permite conocer simultáneamente:

- Qué actor participa.
    
- En qué película participa.
    
- Qué personaje interpreta.
    

### ¿Por qué no utilizar únicamente relaciones binarias?

Porque varias relaciones binarias independientes no siempre permiten representar correctamente una asociación conjunta entre tres entidades.

**Ejemplo: empresa de transporte.**

Tenemos:

- CONDUCTOR.
    
- AUTOBÚS.
    
- RUTA.
    

Queremos conocer qué conductor realiza cada ruta utilizando qué autobús.

|Conductor|Autobús|Ruta|
|---|---|---|
|Alberto|Autobús 1|Madrid-Toledo|
|Alberto|Autobús 2|Madrid-Segovia|
|Carlos|Autobús 1|Madrid-Segovia|

Si utilizamos únicamente relaciones binarias, podríamos conocer:

- Qué autobuses conduce Alberto.
    
- Qué rutas realiza Alberto.
    
- Qué autobuses circulan por cada ruta.
    

Pero no necesariamente qué combinación exacta de conductor, autobús y ruta corresponde a cada servicio.

Una relación ternaria llamada **REALIZA_SERVICIO** permite almacenar las tres entidades conjuntamente.

**Concepto clave:** las relaciones ternarias se utilizan cuando la asociación depende simultáneamente de tres entidades y no puede representarse correctamente mediante relaciones binarias independientes.

---

## Diferencia entre grado y cardinalidad

Aunque están relacionados, **grado y cardinalidad son conceptos diferentes**.

### Grado

Indica el número de entidades que participan en una relación.

Ejemplos:

- Grado 1 → Unaria.
    
- Grado 2 → Binaria.
    
- Grado 3 → Ternaria.
    

### Cardinalidad

Indica cuántas instancias de una entidad pueden asociarse con instancias de otra, según las reglas del sistema.

En relaciones binarias, los tipos habituales son:

|Cardinalidad|Nombre|Ejemplo|
|---|---|---|
|1:1|Uno a uno|Persona — DNI|
|1|Uno a muchos|Departamento — Empleado|
|N|Muchos a muchos|Alumno — Asignatura|

### Ejemplo

`PROFESOR (1) — IMPARTE — (N) ASIGNATURA`

Suponiendo que un profesor puede impartir varias asignaturas y cada asignatura tiene un único profesor:

- **Grado:** 2, porque participan dos entidades.
    
- **Cardinalidad:** 1, porque un profesor puede impartir varias asignaturas.
    

### Tabla comparativa

|Característica|Grado|Cardinalidad|
|---|---|---|
|¿Qué indica?|Número de entidades participantes.|Número de instancias que pueden asociarse.|
|Tipos habituales|Unaria, binaria, ternaria.|1:1, 1, N.|
|¿Qué analiza?|Estructura de la relación.|Cantidad de asociaciones permitidas.|

**Importante para el examen:** una relación binaria puede tener cardinalidad 1:1, 1 o N. El grado no determina la cardinalidad.

---

## Diferencia entre atributo y relación

Es importante distinguir cuándo una información debe representarse como un atributo y cuándo como una relación.

### Atributo

Un **atributo** representa una propiedad o característica de una entidad.

**Ejemplo:**

Entidad: ALUMNO.

Atributos:

- Nombre.
    
- Apellidos.
    
- Fecha de nacimiento.
    
- Nacionalidad.
    

Estos elementos describen al alumno, por lo que son atributos.

### Relación

Una **relación** representa una asociación entre entidades.

**Ejemplo:**

`ALUMNO — CURSA — ASIGNATURA`

CURSA es una relación porque conecta las entidades ALUMNO y ASIGNATURA.

### Cuidado con el verbo «tener»

No todas las expresiones que utilizan el verbo _tener_ representan relaciones.

**Ejemplos de atributos:**

- Un alumno tiene un nombre.
    
- Un alumno tiene una nacionalidad.
    
- Una película tiene un año de estreno.
    

Nombre, nacionalidad y año de estreno son atributos en estos ejemplos.

**Ejemplo de relación:**

- Un alumno tiene asignadas varias asignaturas.
    

Aquí existe una asociación entre ALUMNO y ASIGNATURA.

Por tanto, podemos representarla mediante una relación.

**Regla práctica:**

- Si describe una característica de una entidad → normalmente es un atributo.
    
- Si conecta dos o más entidades → normalmente es una relación.
    

La decisión final depende de los requisitos del sistema.

---

## ¿Cómo identificar las relaciones en un ejercicio?

Para identificar correctamente las relaciones en un enunciado, podemos seguir estos pasos.

### Paso 1. Identificar las entidades

Buscar los objetos o conceptos principales sobre los que necesitamos almacenar información.

### Paso 2. Identificar los atributos

Determinar qué características describen cada entidad.

### Paso 3. Identificar las relaciones

Buscar las asociaciones existentes entre entidades.

Normalmente se expresan mediante verbos como:

- CURSA.
    
- IMPARTE.
    
- DIRIGE.
    
- REALIZA.
    
- PERTENECE.
    
- TRABAJA EN.
    

### Paso 4. Determinar el grado

Contar cuántas entidades participan en cada relación.

- Una entidad → Grado 1.
    
- Dos entidades → Grado 2.
    
- Tres entidades → Grado 3.
    

### Paso 5. Determinar la cardinalidad

Analizar cuántas instancias pueden asociarse según las reglas del sistema.

No debemos suponer una cardinalidad si el enunciado no proporciona información suficiente.

---

## Conceptos clave para el examen

|Concepto|Definición|
|---|---|
|Relación|Asociación entre dos o más entidades.|
|Representación de relación|Rombo conectado mediante líneas a las entidades.|
|Grado|Número de entidades participantes en una relación.|
|Relación unaria|Relación de una entidad consigo misma.|
|Relación binaria|Relación entre dos entidades.|
|Relación ternaria|Relación conjunta entre tres entidades.|
|Relación recursiva|Relación en la que una entidad participa consigo misma.|
|Rol|Función que desempeña una entidad dentro de una relación.|
|Cardinalidad|Número de instancias que pueden asociarse según las reglas del sistema.|

### Ideas fundamentales

1. **Las relaciones representan asociaciones entre entidades.**
    
2. **En el modelo ER clásico, las relaciones se representan mediante rombos.**
    
3. **El nombre de una relación suele expresarse mediante un verbo.**
    
4. **El grado indica el número de entidades participantes.**
    
5. **Las relaciones unarias conectan una entidad consigo misma.**
    
6. **Las relaciones binarias conectan dos entidades.**
    
7. **Las relaciones ternarias conectan tres entidades simultáneamente.**
    
8. **Las relaciones ternarias no siempre pueden sustituirse por relaciones binarias independientes.**
    
9. **El grado y la cardinalidad son conceptos diferentes.**
    
10. **Los atributos describen características; las relaciones representan asociaciones.**
    
11. **No todo lo expresado mediante el verbo «tener» constituye una relación.**
    
12. **Para determinar la cardinalidad debemos analizar las reglas del sistema.**

# 4. Modelo entidad-relación: Cardinalidades y restricciones

## ¿Qué es la cardinalidad?

La **cardinalidad** indica cuántas instancias de una entidad pueden o deben relacionarse con instancias de otra entidad.

Permite establecer restricciones sobre las relaciones existentes entre las entidades de una base de datos.

Para determinar la cardinalidad debemos analizar las reglas del sistema.

Existen dos tipos:

- **Cardinalidad máxima:** indica el número máximo de instancias con las que puede relacionarse una instancia.
    
- **Cardinalidad mínima:** indica el número mínimo de instancias con las que debe relacionarse una instancia.
    

**Ejemplo:**

Tenemos las entidades ALUMNO y ASIGNATURA, relacionadas mediante CURSA.

Debemos determinar:

- ¿Cuántas asignaturas puede cursar un alumno?
    
- ¿Cuántos alumnos pueden cursar una asignatura?
    
- ¿Es obligatorio que un alumno curse alguna asignatura?
    
- ¿Puede existir una asignatura sin alumnos matriculados?
    

Las respuestas permiten establecer las cardinalidades de la relación.

---

## 4.1. Cardinalidad máxima

La **cardinalidad máxima** determina el número máximo de instancias de una entidad con las que puede relacionarse una instancia de otra entidad.

En las relaciones binarias existen tres tipos principales.

### 1. Relación 1:1 (uno a uno)

Una relación **1:1** significa que cada instancia de una entidad puede relacionarse, como máximo, con una instancia de la otra entidad, y viceversa.

**Ejemplo: PROFESOR — TUTORIZA — GRUPO**

Suponiendo que:

- Un profesor puede ser tutor de un único grupo como máximo.
    
- Cada grupo puede tener un único profesor tutor como máximo.
    

La cardinalidad máxima será **1:1**.

**Importante:** una cardinalidad máxima 1:1 no significa necesariamente que la participación sea obligatoria. Eso depende de la cardinalidad mínima.

### 2. Relación 1 (uno a muchos)

Una relación **1** significa que una instancia de una entidad puede relacionarse con varias instancias de otra, mientras que cada instancia de esta última puede relacionarse, como máximo, con una de la primera.

**Ejemplo: PROFESOR — IMPARTE — ASIGNATURA**

Suponiendo que:

- Un profesor puede impartir varias asignaturas.
    
- Cada asignatura tiene un único profesor responsable como máximo.
    

La cardinalidad máxima será **1**.

**Ejemplo de datos:**

|Profesor|Asignatura|
|---|---|
|Carlos|Bases de Datos|
|Carlos|Sistemas Operativos|
|Carlos|Redes|
|María|Lenguajes de Marcas|

Un profesor puede aparecer asociado a varias asignaturas.

### 3. Relación N (muchos a muchos)

Una relación **N** significa que varias instancias de una entidad pueden relacionarse con varias instancias de otra.

**Ejemplo: ALUMNO — CURSA — ASIGNATURA**

Suponiendo que:

- Un alumno puede cursar varias asignaturas.
    
- Una asignatura puede tener varios alumnos.
    

La cardinalidad máxima será **N**.

**Ejemplo:**

|Alumno|Asignatura|
|---|---|
|Alberto|Bases de Datos|
|Alberto|Sistemas Operativos|
|María|Bases de Datos|
|María|Redes|

Alberto puede cursar varias asignaturas y Bases de Datos puede tener varios alumnos.

### Resumen de cardinalidades máximas

|Cardinalidad|Nombre|Significado|
|---|---|---|
|1:1|Uno a uno|Una instancia se relaciona como máximo con una de la otra entidad, en ambos sentidos.|
|1|Uno a muchos|Una instancia puede relacionarse con varias de la otra entidad.|
|N|Muchos a muchos|Varias instancias pueden relacionarse con varias de la otra entidad.|

**Importante:** las cardinalidades máximas indican límites, pero no determinan si la participación es obligatoria.

---

## 4.2. Cardinalidad mínima

La **cardinalidad mínima** indica el número mínimo de instancias de otra entidad con las que debe relacionarse una instancia.

Los valores habituales son:

- **0:** participación opcional.
    
- **1:** participación obligatoria.
    

### Cardinalidad mínima 0 (opcional)

Significa que una instancia puede existir sin participar en la relación.

**Ejemplo:**

Un profesor puede estar registrado en el sistema sin tener asignada ninguna asignatura.

Por tanto, su participación en la relación IMPARTE puede ser opcional.

### Cardinalidad mínima 1 (obligatoria)

Significa que una instancia debe participar al menos una vez en la relación.

**Ejemplo:**

En una tienda online, cada pedido debe pertenecer obligatoriamente a un cliente.

Por tanto, la participación de PEDIDO en la relación con CLIENTE es obligatoria.

### Diferencia entre cardinalidad mínima y máxima

|Cardinalidad|¿Qué indica?|
|---|---|
|Mínima|Número mínimo de asociaciones obligatorias.|
|Máxima|Número máximo de asociaciones permitidas.|

### Combinaciones de cardinalidad mínima y máxima

La cardinalidad completa se expresa mediante:

**(Mínimo, Máximo)**

Existen cuatro combinaciones habituales:

|Cardinalidad|Significado|
|---|---|
|(0,1)|Puede relacionarse con cero o una instancia.|
|(1,1)|Debe relacionarse exactamente con una instancia.|
|(0,N)|Puede relacionarse con cero, una o muchas instancias.|
|(1,N)|Debe relacionarse con una o muchas instancias.|

#### (0,1): opcional, máximo uno

**Ejemplo:** un empleado puede tener asignada una plaza de aparcamiento o ninguna.

- Mínimo: 0.
    
- Máximo: 1.
    

#### (1,1): obligatorio, exactamente uno

**Ejemplo:** cada pedido debe pertenecer a un único cliente.

- Mínimo: 1.
    
- Máximo: 1.
    

#### (0,N): opcional, muchos

**Ejemplo:** un cliente puede realizar muchos pedidos o ninguno.

- Mínimo: 0.
    
- Máximo: N.
    

#### (1,N): obligatorio, muchos

**Ejemplo:** en un instituto donde es obligatorio matricularse, cada alumno debe cursar al menos una asignatura y puede cursar varias.

- Mínimo: 1.
    
- Máximo: N.
    

**Concepto clave:** el valor mínimo indica si la participación es obligatoria u opcional, mientras que el máximo indica cuántas asociaciones se permiten.

---

## 4.3. Representación gráfica de las cardinalidades

Existen diferentes notaciones para representar gráficamente las cardinalidades en un diagrama entidad-relación.

Las dos estudiadas en el temario son:

1. **Notación clásica de Chen.**
    
2. **Notación pata de gallo (Crow's Foot).**
    

### 1. Notación clásica de Chen

En esta notación:

- Las entidades se representan mediante rectángulos.
    
- Las relaciones se representan mediante rombos.
    
- Los atributos se representan mediante elipses.
    
- Las cardinalidades se indican mediante números o letras junto a las conexiones.
    

**Ejemplo: PELÍCULA — RODAJE — DIRECTOR**

Supongamos que:

- Cada película debe tener exactamente un director.
    
- Un director puede dirigir muchas películas.
    
- Un director puede existir sin haber dirigido ninguna película.
    

La cardinalidad máxima es **1**.

La cardinalidad completa es:

- Una película se relaciona con **(1,1) directores**.
    
- Un director se relaciona con **(0,N) películas**.
    

Siguiendo la representación utilizada en el temario:

`PELÍCULA (0,N) — RODAJE — (1,1) DIRECTOR`

**Importante:** en esta representación, la cardinalidad situada junto a una entidad indica cuántas instancias de esa entidad pueden relacionarse con una instancia de la entidad opuesta.

Por eso:

- (0,N), junto a PELÍCULA, indica cuántas películas puede dirigir un director.
    
- (1,1), junto a DIRECTOR, indica cuántos directores puede tener una película.
    

Para evitar errores, debemos leer siempre la relación en ambos sentidos.

### 2. Notación pata de gallo (Crow's Foot)

La **notación pata de gallo** representa las cardinalidades mediante símbolos colocados en los extremos de las líneas que conectan las entidades.

Utiliza tres símbolos fundamentales:

|Símbolo|Significado|
|---|---|
|Círculo (O)|Participación opcional: mínimo 0.|
|Barra (\|)|Uno: se utiliza para indicar mínimo o máximo 1.|
|Pata de gallo|Muchos: máximo N.|

### Combinaciones de símbolos

|Representación simplificada|Cardinalidad|Significado|
|---|---|---|
|O\||(0,1)|Cero o uno.|
|\||(1,1)|Exactamente uno.|
|O<|(0,N)|Cero o muchos.|
|\|<|(1,N)|Uno o muchos.|

El símbolo `<` representa de forma simplificada la pata de gallo.

**Ejemplo: CLIENTE — REALIZA — PEDIDO**

Suponiendo que:

- Un cliente puede realizar cero o muchos pedidos.
    
- Cada pedido pertenece obligatoriamente a un único cliente.
    

Las cardinalidades serán:

- CLIENTE respecto a PEDIDO: (0,N).
    
- PEDIDO respecto a CLIENTE: (1,1).
    

En el diagrama pata de gallo, el extremo próximo a PEDIDO mostraría cero o muchos, y el extremo próximo a CLIENTE mostraría exactamente uno.

---

## 4.4. Atributos en las relaciones N

### ¿Pueden las relaciones tener atributos?

**Sí. Una relación puede tener atributos propios cuando una característica depende de la asociación entre entidades y no de una entidad individual.**

Esto es especialmente habitual en las relaciones N.

### Ejemplo: ACTOR — INTERPRETA — PELÍCULA

Tenemos dos entidades.

**PELÍCULA**

- Código.
    
- Nombre.
    
- Género.
    
- Año.
    
- Formato.
    

**ACTOR**

- Código.
    
- Nombre.
    
- Nacionalidad.
    

Entre ellas existe una relación N porque:

- Un actor puede participar en muchas películas.
    
- Una película puede tener muchos actores.
    

Ahora necesitamos almacenar qué personaje interpreta cada actor en cada película.

### ¿Dónde almacenamos PERSONAJE?

No sería adecuado colocarlo como atributo exclusivo de ACTOR porque un mismo actor puede interpretar diferentes personajes en distintas películas.

Tampoco sería adecuado colocarlo como atributo exclusivo de PELÍCULA porque una película puede contener numerosos personajes interpretados por diferentes actores.

Por tanto, **PERSONAJE puede representarse como un atributo de la relación INTERPRETA**.

**Ejemplo:**

|Actor|Película|Personaje|
|---|---|---|
|Robert Downey Jr.|Iron Man|Tony Stark|
|Robert Downey Jr.|Sherlock Holmes|Sherlock Holmes|
|Christian Bale|The Dark Knight|Bruce Wayne|

El valor de PERSONAJE depende de la combinación de actor y película.

### Representación en el modelo ER

En la notación clásica:

- ACTOR se representa mediante un rectángulo.
    
- PELÍCULA se representa mediante otro rectángulo.
    
- INTERPRETA se representa mediante un rombo.
    
- PERSONAJE se representa mediante una elipse conectada al rombo.
    

**Importante:** un atributo de una relación describe una característica de la asociación, no necesariamente de las entidades por separado.

### Otros ejemplos de atributos de relaciones

|Entidades|Relación|Atributo|
|---|---|---|
|ALUMNO — ASIGNATURA|CURSA|Nota|
|EMPLEADO — PROYECTO|PARTICIPA|Horas trabajadas|
|PRODUCTO — PEDIDO|CONTIENE|Cantidad|
|ACTOR — PELÍCULA|INTERPRETA|Personaje|

**Ejemplo con alumnos:**

Un alumno puede cursar varias asignaturas y una asignatura puede tener varios alumnos.

La nota depende de qué alumno cursa qué asignatura.

Por tanto, NOTA puede ser un atributo de la relación CURSA.

### Transformación de una relación N al modelo relacional

Cuando una relación N se transforma en tablas de una base de datos relacional, normalmente se crea una **tabla intermedia**.

Por ejemplo:

**ALUMNO**

|ID_Alumno|Nombre|
|---|---|
|1|Alberto|
|2|María|

**ASIGNATURA**

|ID_Asignatura|Nombre|
|---|---|
|10|Bases de Datos|
|20|Redes|

**MATRÍCULA**

|ID_Alumno|ID_Asignatura|Nota|
|---|---|---|
|1|10|8|
|1|20|7|
|2|10|9|

La tabla MATRÍCULA permite:

- Relacionar alumnos con asignaturas.
    
- Representar la relación N.
    
- Almacenar el atributo NOTA.
    

En este ejemplo, la combinación ID_Alumno + ID_Asignatura podría utilizarse como clave primaria compuesta si cada alumno solo puede tener una matrícula por asignatura.

**Importante:** una relación con atributos puede representarse como una entidad asociativa durante el diseño, especialmente al transformar el modelo conceptual en un modelo relacional.

---

## Diferencia entre grado y cardinalidad

Estos conceptos no deben confundirse.

|Concepto|Definición|Ejemplo|
|---|---|---|
|Grado|Número de entidades participantes en una relación.|Binaria: dos entidades.|
|Cardinalidad máxima|Número máximo de instancias relacionadas.|1.|
|Cardinalidad mínima|Número mínimo de instancias relacionadas.|0 o 1.|

**Ejemplo:**

`PROFESOR — IMPARTE — ASIGNATURA`

Suponiendo que un profesor puede impartir varias asignaturas y cada asignatura tiene un único profesor:

- **Grado:** 2.
    
- **Cardinalidad máxima:** 1.
    
- **Cardinalidad mínima:** dependerá de si es obligatorio que los profesores impartan asignaturas y de si todas las asignaturas deben tener profesor.
    

---

## Conceptos clave para el examen

|Concepto|Definición|
|---|---|
|Cardinalidad|Cantidad de instancias que pueden o deben asociarse.|
|Cardinalidad máxima|Número máximo de instancias relacionadas.|
|Cardinalidad mínima|Número mínimo de instancias relacionadas.|
|1:1|Relación uno a uno.|
|1|Relación uno a muchos.|
|N|Relación muchos a muchos.|
|(0,1)|Participación opcional, máximo una instancia.|
|(1,1)|Participación obligatoria, exactamente una instancia.|
|(0,N)|Participación opcional, múltiples instancias posibles.|
|(1,N)|Participación obligatoria, múltiples instancias posibles.|
|Notación de Chen|Representa entidades, atributos y relaciones mediante figuras geométricas.|
|Pata de gallo|Representa cardinalidades mediante círculos, barras y ramificaciones.|
|Atributo de relación|Característica que depende de una asociación entre entidades.|
|Tabla intermedia|Tabla utilizada habitualmente para implementar relaciones N.|

### Ideas fundamentales

1. **La cardinalidad indica cuántas instancias pueden o deben relacionarse.**
    
2. **La cardinalidad máxima determina si una relación es 1:1, 1 o N.**
    
3. **La cardinalidad mínima indica si la participación es opcional u obligatoria.**
    
4. **El valor 0 representa participación opcional.**
    
5. **El valor 1 como mínimo representa participación obligatoria.**
    
6. **Las cardinalidades completas se expresan mediante (mínimo, máximo).**
    
7. **Las combinaciones habituales son (0,1), (1,1), (0,N) y (1,N).**
    
8. **La cardinalidad debe determinarse leyendo las reglas del sistema en ambos sentidos.**
    
9. **La notación pata de gallo utiliza círculos, barras y ramificaciones.**
    
10. **Las relaciones N pueden tener atributos propios.**
    
11. **Un atributo de relación describe la asociación entre entidades.**
    
12. **Las relaciones N suelen implementarse mediante tablas intermedias en el modelo relacional.**
    
13. **El grado y la cardinalidad son conceptos diferentes.**