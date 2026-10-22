## 1. ¿Qué es un sistema operativo (SO)?

**Definición:** un **sistema operativo (SO o SSOO en plural)** es el conjunto de programas que **administra los recursos de hardware** y permite ejecutar aplicaciones y realizar tareas.

El libro compara el SO con un **director de orquesta**: coordina los componentes y decide qué proceso utiliza cada recurso en cada momento, evitando conflictos.

### Conceptos fundamentales

- **Hardware (HW):** componentes físicos del equipo: CPU, RAM, discos y periféricos.
- **Software:** programas e instrucciones que utiliza el ordenador.
- **Proceso:** programa en ejecución junto con la información de contexto necesaria para funcionar.
- **Concurrencia:** capacidad de progresar en varias tareas durante un mismo periodo, aunque no todas se ejecuten literalmente al mismo instante. **Aclaración.**
- **Planificación de CPU:** elección de qué proceso o hilo utilizará el procesador.
- **Quantum:** intervalo de tiempo de CPU asignado a una tarea en ciertos algoritmos de planificación.

**Ejemplo:** mientras escuchas música y navegas por Internet, el SO organiza el uso del procesador, la memoria y los dispositivos de ambas aplicaciones.

> [!important] Para el examen  
> El SO **administra los recursos**, **planifica la CPU** y **coordina procesos concurrentes**.

## 2. Evolución histórica: cuatro generaciones

**Definición:** la evolución de los SO está ligada a los avances del hardware: equipos más pequeños, potentes y eficientes.

|Generación|Época según el libro|Tecnología|Programación y características|
|---|---|---|---|
|Primera|Hasta 1955|Tubos de vacío|Código máquina; paneles cableados y tarjetas perforadas|
|Segunda|Hasta 1965|Transistores|Ensamblador o FORTRAN; trabajos por lotes|
|Tercera|Hasta 1980|Circuitos integrados|UNIX, tiempo compartido y multiprogramación; BASIC, C, PASCAL|
|Cuarta|Hasta la actualidad|Integración creciente de circuitos|Windows, macOS y GNU/Linux; multitarea y redes|

### Definiciones que debes conocer

- **Tubo de vacío:** componente electrónico utilizado en los primeros ordenadores antes de la generalización del transistor.
- **Transistor:** componente semiconductor empleado para controlar señales eléctricas, más pequeño y eficiente que los tubos de vacío en muchas aplicaciones.
- **Circuito integrado:** conjunto de componentes electrónicos fabricados sobre un mismo chip.
- **Código máquina:** instrucciones binarias que ejecuta directamente un procesador.
- **Ensamblador:** lenguaje de bajo nivel próximo a las instrucciones de la CPU.
- **Tarjeta perforada:** soporte físico que codifica información mediante perforaciones.
- **Procesamiento por lotes (_batch_):** ejecución de trabajos agrupados sin intervención continua del usuario.
- **Multiprogramación:** presencia de varios programas en memoria para mejorar el aprovechamiento de la CPU.
- **Tiempo compartido:** reparto del tiempo de CPU entre tareas o usuarios para permitir interacción.
- **Multitarea:** capacidad del SO para gestionar varias tareas durante un mismo periodo.

**Aclaración:** la tabla presenta la periodización utilizada en el libro; los cambios tecnológicos históricos fueron graduales, no fronteras exactas.

## 3. Arquitectura de los sistemas operativos

**Definición:** la **arquitectura de un SO** es la forma en que se organizan sus componentes y subsistemas, y cómo se relacionan para prestar servicios.

El libro explica que los sistemas evolucionaron desde diseños **monolíticos** hacia una organización con **subsistemas especializados**, aplicando la idea de «divide y vencerás».

- **Diseño monolítico:** muchas funciones principales del sistema se ejecutan dentro de un mismo núcleo.
- **Organización modular o por capas:** separación conceptual o estructural de responsabilidades para facilitar su organización.

**Aclaración:** monolítico y modular no son categorías totalmente excluyentes; existen núcleos monolíticos que admiten módulos.

### 3.1. Subsistemas internos

Son los componentes encargados de realizar las funciones centrales del SO.

#### A. Núcleo o kernel

**Definición:** parte central del sistema operativo que controla recursos esenciales, gestiona la ejecución privilegiada y coordina servicios del sistema.

**Funciones destacadas en el libro:** planificación y prioridades de CPU, atención a interrupciones y coordinación de subsistemas.

- **Interrupción:** señal que requiere atención del procesador, por ejemplo cuando termina una operación de hardware. **Aclaración.**
- **HAL (_Hardware Abstraction Layer_):** capa de abstracción que proporciona una interfaz para trabajar con características del hardware sin depender de todos sus detalles.

**Ejemplo:** el SO atiende una interrupción de un dispositivo y activa el código correspondiente.

#### B. Gestión de procesos

**Definición:** subsistema que administra los programas en ejecución y decide cómo se reparte la CPU entre ellos.

- **Planificador:** selecciona las tareas que van a ejecutarse.
- **Algoritmo de planificación:** conjunto de reglas para elegir el orden y el tiempo de ejecución.
- **Rotación o _round robin_:** algoritmo que distribuye turnos de CPU entre tareas listas; normalmente emplea un quantum. **Aclaración.**
- **Prioridad:** criterio que puede influir en el orden de ejecución.

**Ejemplo:** el SO alterna entre un editor, un navegador y un reproductor de audio.

#### C. Gestión del almacenamiento primario y secundario

**Definición:** subsistema que organiza dónde se mantienen los datos y la información necesaria para ejecutar procesos.

- **Almacenamiento primario:** principalmente **memoria RAM**, rápida y volátil.
- **Almacenamiento secundario:** SSD, HDD y otros soportes que mantienen datos de forma persistente.
- **Memoria virtual:** mecanismo para gestionar direcciones de memoria de los procesos y su correspondencia con memoria física.
- **Intercambio o _swapping_:** traslado de información entre RAM y un área de almacenamiento secundario para gestionar la presión de memoria; el libro lo relaciona con procesos que llevan tiempo sin activarse.

**Ejemplo:** si la RAM está muy ocupada, el SO puede desplazar páginas de memoria poco utilizadas a un área de intercambio.

> [!warning] Diferencia importante  
> **RAM ≠ SSD/HDD.** El intercambio ayuda a gestionar memoria, pero el almacenamiento secundario es normalmente mucho más lento que la RAM. **Aclaración.**

#### D. Gestión de entrada/salida (E/S)

**Definición:** subsistema que controla la comunicación entre el sistema operativo y los dispositivos de hardware.

- **Driver o controlador:** software que permite al SO comunicarse con un dispositivo concreto.
- **Dispositivo de entrada:** introduce información, como teclado o ratón.
- **Dispositivo de salida:** presenta resultados, como pantalla o impresora.

**Ejemplo:** al pulsar una tecla, el controlador y el sistema de E/S participan en el tratamiento de esa entrada.

#### E. Sistema de archivos

**Definición:** subsistema que organiza los archivos y directorios y permite **guardar, localizar y recuperar datos** en soportes de almacenamiento.

**Funciones:** manejar rutas, acceder a archivos y recuperar información desde almacenamiento local o remoto, según el soporte y los servicios disponibles.

**Ejemplo:** abrir `/home/usuario/apuntes.md` en Linux o `C:\Usuarios\Alumno\apuntes.md` en Windows.

#### F. Sistemas de protección

**Definición:** mecanismos que controlan qué usuarios y procesos pueden acceder a determinados recursos.

**Objetivo:** impedir accesos sin permiso y reducir el riesgo de errores o acciones maliciosas.

**Ejemplo:** un proceso sin privilegios no debería modificar libremente los archivos protegidos del sistema.

#### G. Sistemas de comunicaciones

**Definición:** subsistema que gestiona la comunicación del equipo con otros sistemas a través de adaptadores de red y protocolos.

- **Pila de protocolos:** conjunto de protocolos organizados que permiten intercambiar datos.
- **TCP/IP:** familia de protocolos utilizada habitualmente en redes e Internet.
- **Adaptador de red:** dispositivo que conecta un equipo a una red cableada o inalámbrica.

**Ejemplo:** al abrir una página web, el SO utiliza sus funciones de red para enviar y recibir datos.

### Tabla de subsistemas internos

|Subsistema|Función principal|
|---|---|
|Núcleo|Coordinar funciones centrales y recursos|
|Procesos|Crear, organizar y planificar tareas|
|Memoria y almacenamiento|Gestionar RAM, memoria virtual y almacenamiento|
|Entrada/salida|Comunicar programas y dispositivos|
|Archivos|Organizar, guardar y recuperar información|
|Protección|Controlar permisos y accesos|
|Comunicaciones|Gestionar redes y protocolos|

## 4. Subsistemas externos: interfaces de usuario

**Definición:** mecanismos mediante los que una persona **interactúa con el sistema operativo** para ejecutar acciones y acceder a sus funciones.

### 4.1. CLI — Interfaz de línea de comandos

**Definición:** _Command-Line Interface_. Interfaz **textual** en la que el usuario introduce órdenes para controlar el sistema.

**Características del libro:** es una forma histórica de interacción y continúa siendo útil para tareas automatizadas y procesos por lotes.

**Ejemplos:** Bash en Linux, PowerShell y CMD en Windows.

**Ejemplo de orden:** `dir` en CMD o `ls` en Bash para listar archivos.

### 4.2. GUI — Interfaz gráfica de usuario

**Definición:** _Graphical User Interface_. Interfaz que permite interactuar mediante **ventanas, iconos, menús y elementos visuales**.

**Conceptos relacionados:**

- **Entorno de escritorio (DE):** conjunto de componentes que proporciona una experiencia gráfica de trabajo.
- **Servidor de pantalla:** componente que participa en la presentación gráfica y la comunicación con los dispositivos de entrada, según la arquitectura utilizada. **Aclaración.**
- **Gestor de ventanas:** administra la posición, tamaño y comportamiento de las ventanas.

**Ejemplos:** escritorio de Windows, GNOME o KDE Plasma.

### 4.3. NUI — Interfaz natural de usuario

**Definición:** _Natural User Interface_. Interfaz que busca permitir una interacción más **natural e intuitiva**, por ejemplo mediante lenguaje hablado o gestos. El libro destaca los asistentes basados en lenguaje natural.

**Ejemplo:** solicitar por voz a un asistente que abra una aplicación.

### Comparativa CLI, GUI y NUI

|Interfaz|Forma principal de interacción|Ejemplo|Ventaja habitual|
|---|---|---|---|
|CLI|Órdenes escritas|PowerShell, Bash|Automatización y control preciso|
|GUI|Elementos visuales|Escritorio Windows|Facilidad de uso visual|
|NUI|Lenguaje natural u otras interacciones intuitivas|Asistente de voz|Interacción más directa|

_La columna de ventajas es una ampliación didáctica._

## 5. Ejemplo práctico: abrir un archivo desde el escritorio

1. **GUI:** haces doble clic en el icono.
2. **Gestión de procesos:** el SO inicia o activa la aplicación correspondiente.
3. **Gestión de memoria:** asigna recursos para ejecutar el programa.
4. **Sistema de archivos:** localiza los datos solicitados.
5. **E/S y drivers:** se comunica con el almacenamiento y la pantalla.
6. **Protección:** comprueba los permisos necesarios.

_Ejemplo explicativo: no describe una secuencia obligatoria exacta de operaciones internas._

## 6. Conceptos clave para el examen

- **SO:** coordina recursos y ejecución de programas.
- **Proceso:** programa en ejecución con su contexto.
- **Quantum:** turno de CPU usado en determinados algoritmos.
- **Kernel:** parte central del SO.
- **HAL:** abstracción del hardware.
- **Scheduler:** planificador de tareas en CPU.
- **Swapping:** intercambio de información entre RAM y almacenamiento secundario.
- **Driver:** software para controlar dispositivos.
- **Sistema de archivos:** organización y recuperación de archivos.
- **TCP/IP:** familia de protocolos de comunicación en red.
- **CLI:** comandos de texto.
- **GUI:** interacción gráfica.
- **NUI:** interacción natural.

## 7. Preguntas de autoevaluación

1. ¿Por qué se compara el SO con un director de orquesta?
2. ¿Qué es un quantum y qué relación tiene con la planificación?
3. ¿Qué diferencia hay entre un proceso y una aplicación almacenada?
4. ¿Qué función tiene el kernel?
5. ¿En qué consiste el swapping?
6. ¿Qué es un driver y a qué subsistema pertenece?
7. ¿Qué función desempeña TCP/IP?
8. ¿Qué diferencia hay entre CLI, GUI y NUI?
9. ¿Qué tecnologías caracterizan la segunda y tercera generaciones del libro?
10. ¿Qué subsistema comprueba si un proceso puede acceder a un recurso?