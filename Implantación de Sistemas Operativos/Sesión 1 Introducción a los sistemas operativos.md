## 1. ¿Qué es un sistema operativo (SO)?

**Definición:** un **sistema operativo (SO)** es el conjunto de programas que **administra los recursos físicos (hardware)** de un ordenador y **ofrece servicios a las aplicaciones**, actuando como intermediario entre usuario, programas y dispositivos.

### Dos formas de entenderlo

- **SO como máquina extendida:** oculta detalles complejos del hardware y ofrece abstracciones sencillas como **archivos, procesos y ventanas**.
- **SO como gestor de recursos:** distribuye el uso de **CPU, memoria, almacenamiento y dispositivos** entre los programas de manera organizada y segura.

**Ejemplo:** cuando guardas un archivo, no necesitas conocer los sectores del SSD. El sistema operativo organiza la operación y decide cómo acceder al dispositivo.

> [!important] Para el examen  
> El SO **simplifica el uso del hardware** y **gestiona sus recursos**.

## 2. Niveles de un sistema informático

**Definición:** la estructura en niveles representa las capas que intervienen entre la persona y los componentes físicos del equipo.

|Nivel|¿Qué es?|Ejemplos|
|---|---|---|
|Usuario|Persona que utiliza el sistema|Administrador, estudiante|
|Aplicaciones|Programas que realizan tareas para el usuario|Navegador, editor, IDE|
|Utilidades e intérprete de órdenes|Herramientas para manejar el sistema|Shell, explorador de archivos|
|Núcleo (_kernel_)|Parte central que gestiona procesos, memoria, E/S, archivos y seguridad|Núcleo Linux|
|Hardware|Componentes físicos|CPU, RAM, SSD, teclado|

**Ejemplo:** usuario → editor de texto → servicios del SO → almacenamiento físico.

**Aclaración:** es una representación conceptual; no todas las operaciones recorren literalmente cada capa.

## 3. Breve evolución histórica

- **Años 50 — procesamiento por lotes (_batch_):** trabajos preparados para ejecutarse sin interacción directa durante el procesamiento.
- **Años 60 — multiprogramación y tiempo compartido:** varios programas permanecen activos y la CPU reparte tiempo entre ellos; ejemplos del material: CTSS, MULTICS y OS/360.
- **1969–1970 — UNIX:** surge en Bell Labs y ejerce una gran influencia en sistemas posteriores.
- **Años 80 — ordenador personal:** expansión de MS-DOS, Mac OS e interfaces gráficas.
- **1991 — Linux:** Linus Torvalds publica el núcleo Linux; combinado con herramientas GNU permite sistemas libres completos.
- **1993 — Windows NT:** aparece la familia NT, base de versiones modernas de Windows.
- **Desde 2000 — movilidad y virtualización:** crecimiento de Android, iOS, máquinas virtuales, contenedores y servicios en la nube.

### Conceptos históricos esenciales

- **Procesamiento por lotes:** ejecutar trabajos agrupados sin interacción continua del usuario.
- **Multiprogramación:** mantener varios programas disponibles para aprovechar mejor el procesador.
- **Tiempo compartido:** alternar rápidamente el uso de CPU entre tareas o usuarios para ofrecer respuesta interactiva.

## 4. Funciones principales del sistema operativo

### 4.1. Gestión de procesos

**Proceso:** **programa que se está ejecutando**, con sus recursos y estado de ejecución.

**Gestión de procesos:** función del SO que crea y finaliza procesos, decide cuáles usan la CPU, gestiona hilos y facilita su coordinación.

- **Planificador (_scheduler_):** componente que decide qué proceso o hilo recibe tiempo de CPU.
- **Hilo (_thread_):** unidad de ejecución dentro de un proceso; varios hilos pueden compartir recursos del mismo proceso. **Ampliación.**
- **Sincronización:** mecanismos para coordinar actividades concurrentes; el material cita **mutex** y **semáforos**.
- **IPC (_Inter-Process Communication_):** mecanismos de comunicación entre procesos.

#### Estados básicos de un proceso

|Estado|Definición|
|---|---|
|Nuevo|Se está creando|
|Listo|Puede ejecutarse, pero espera tiempo de CPU|
|En ejecución|Sus instrucciones se están ejecutando en CPU|
|Bloqueado / en espera|Espera un evento o recurso, como una operación de E/S|
|Terminado|Ha finalizado|

**Diferencia clave:** un proceso **listo espera CPU**; un proceso **bloqueado espera que suceda algo**, por lo que darle CPU no basta para reanudarlo.

**Ejemplo:** un programa que espera datos del disco puede quedar bloqueado hasta que finalice la lectura.

### 4.2. Gestión de memoria

**Definición:** función del SO que organiza el uso de la **RAM** por parte de los programas y del propio sistema.

**Funciones:**

- Asignar memoria a los procesos.
- Controlar qué zonas puede utilizar cada proceso.
- Permitir compartir datos de forma controlada.
- Recuperar memoria que ya no se necesita.

**Memoria virtual:** mecanismo que ofrece a los procesos un espacio de direcciones virtuales y permite gestionar su relación con la memoria física. **Ampliación:** puede apoyarse en almacenamiento secundario cuando sea necesario; no equivale simplemente a «más RAM».

**Ejemplo:** al abrir varias aplicaciones, el SO asigna y controla la memoria utilizada por cada una.

### 4.3. Gestión de entrada/salida (E/S o I/O)

**Definición:** función que **coordina la comunicación entre programas y dispositivos** como teclado, pantalla, discos, impresoras o adaptadores de red.

**Objetivo:** proporcionar acceso organizado al hardware sin obligar a cada aplicación a conocer todos los detalles de cada dispositivo.

**Ejemplo:** al imprimir, la aplicación solicita la operación y el sistema operativo coordina el acceso a la impresora.

### 4.4. Sistema de archivos

**Definición:** conjunto de **estructuras y reglas** para organizar, guardar y localizar datos mediante **archivos y directorios**.

- Permite utilizar **nombres y rutas** en vez de posiciones físicas del disco.
- Un SO puede admitir **varios sistemas de archivos**: no existe una relación exclusiva de «un sistema operativo = un sistema de archivos».
- El material menciona **NTFS, FAT32 y exFAT** en Windows y el acceso a NTFS desde Linux mediante controladores como **NTFS3**.

**Ejemplo:** una ruta como `Documentos/redes/apuntes.md` permite encontrar un archivo sin saber dónde están sus bloques físicos.

> [!important] Para el examen  
> **Sistema operativo** y **sistema de archivos** no son lo mismo. Windows puede utilizar NTFS, FAT32 y exFAT; otros sistemas también pueden admitir algunos de ellos.

### 4.5. Seguridad y protección

**Definición:** funciones destinadas a impedir **accesos no autorizados, usos indebidos y daños** en datos y recursos, ya sea por errores o por acciones maliciosas.

**Medidas citadas:** identificación de usuarios, control de permisos y establecimiento de límites para los programas.

**Ejemplo:** un usuario sin permisos de administrador no debería poder modificar ciertos archivos protegidos del sistema.

## 5. Relación entre las funciones

**Situación práctica:** abres un navegador y descargas un archivo.

1. **Procesos:** el SO gestiona la ejecución del navegador.
2. **Memoria:** reserva RAM para sus datos.
3. **E/S:** coordina la comunicación con el adaptador de red y el disco.
4. **Archivos:** guarda el documento con un nombre y una ruta.
5. **Seguridad:** comprueba los permisos necesarios para acceder al destino.

_Este ejemplo integra los conceptos explicados; no es una secuencia literal de llamadas internas._

## 6. Repaso rápido para el examen

|Concepto|Qué debes recordar|
|---|---|
|Sistema operativo|Gestiona hardware y proporciona servicios a aplicaciones|
|Máquina extendida|Oculta la complejidad del hardware|
|Gestor de recursos|Reparte CPU, RAM, almacenamiento y dispositivos|
|Kernel|Parte central del SO|
|Proceso|Programa en ejecución|
|Scheduler|Decide qué tarea recibe CPU|
|Listo|Espera CPU|
|Bloqueado|Espera evento o recurso|
|Gestión de memoria|Asigna, controla y recupera memoria|
|E/S|Comunicación con dispositivos|
|Sistema de archivos|Organización de archivos y directorios|
|Protección|Usuarios, permisos y límites|

## 7. Preguntas de autoevaluación

1. ¿Qué diferencia hay entre el SO como máquina extendida y como gestor de recursos?
2. ¿Qué es un proceso y en qué se diferencia de un programa almacenado?
3. ¿Qué distingue un proceso listo de uno bloqueado?
4. ¿Qué función desempeña el planificador?
5. ¿Por qué un sistema operativo puede utilizar varios sistemas de archivos?
6. ¿Qué recursos protege la gestión de seguridad?

> [!note] Alcance del PDF  
> El índice del documento menciona **modos de ejecución, llamadas al sistema y arquitecturas del núcleo**, pero las páginas facilitadas **no desarrollan esos apartados**. No se incluyen como contenido explicado de esta sesión para evitar atribuirles información no presente.