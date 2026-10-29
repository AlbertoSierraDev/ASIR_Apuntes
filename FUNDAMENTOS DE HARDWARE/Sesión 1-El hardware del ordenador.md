# 1. Sistema informático y sus elementos funcionales

## 1.1. ¿Qué es un sistema informático?

Un **sistema informático** es el conjunto de elementos físicos, programas, datos, usuarios y procedimientos que trabajan de forma coordinada para **capturar, procesar, almacenar y comunicar información**.

Su objetivo es transformar datos en información útil para realizar tareas o resolver problemas.

Un sistema informático no está formado únicamente por un ordenador, sino por todos los elementos necesarios para su funcionamiento.

### Elementos principales

|Elemento|Definición|
|---|---|
|Hardware|Componentes físicos del sistema.|
|Software|Programas e instrucciones que controlan el hardware.|
|Datos|Información que el sistema captura, procesa o almacena.|
|Usuarios y procedimientos|Personas que utilizan el sistema y normas que regulan su uso.|

**Ejemplo práctico:**

En un supermercado, el lector de códigos de barras es hardware, el programa de caja es software, los precios son datos y el cajero es el usuario.

---

## 1.2. Hardware

El **hardware** es el conjunto de componentes físicos y tangibles de un sistema informático.

Son los dispositivos que permiten introducir, procesar, almacenar y mostrar información.

### Clasificación del hardware

**Hardware de procesamiento**

Se encarga de ejecutar instrucciones y realizar operaciones.

- CPU (procesador).
    
- GPU (procesador gráfico).
    

**Hardware de almacenamiento**

Permite guardar información.

- HDD (disco duro mecánico).
    
- SSD (unidad de estado sólido).
    
- Memorias USB.
    

**Hardware de entrada**

Permite introducir datos al ordenador.

- Teclado.
    
- Ratón.
    
- Micrófono.
    
- Escáner.
    

**Hardware de salida**

Permite mostrar o reproducir información.

- Monitor.
    
- Impresora.
    
- Altavoces.
    

**Hardware de entrada y salida**

Permite enviar y recibir información.

- Tarjeta de red.
    
- Pantalla táctil.
    
- Dispositivos USB con comunicación bidireccional.
    

> **Importante:** un mismo dispositivo puede desempeñar varias funciones.

---

## 1.3. Software

El **software** es el conjunto de programas e instrucciones que indican al hardware qué operaciones debe realizar.

El software no es físico: está formado por instrucciones y datos almacenados en soportes físicos.

### Tipos de software

|Tipo|Función|Ejemplos|
|---|---|---|
|Software de sistema|Administra recursos y proporciona servicios básicos.|Windows, Linux|
|Software de aplicación|Permite realizar tareas específicas.|Word, Chrome|
|Software de programación|Facilita el desarrollo de programas.|Compiladores, depuradores, IDE|

### Sistema operativo

Un **sistema operativo (SO)** es el software principal que administra los recursos del ordenador y proporciona servicios a las aplicaciones.

Funciones principales:

- Gestionar procesos.
    
- Administrar memoria RAM.
    
- Controlar dispositivos.
    
- Gestionar archivos y almacenamiento.
    
- Administrar usuarios y permisos.
    
- Facilitar la interacción con el ordenador.
    

**Ejemplo:** cuando ejecutamos Chrome, el sistema operativo gestiona su ejecución, la memoria que utiliza y el acceso a los dispositivos.

---

## 1.4. Datos

Los **datos** son representaciones de hechos, valores o contenidos que un sistema informático puede procesar.

Pueden ser:

- Numéricos: `25`, `100`, `3.14`.
    
- Textuales: nombres y documentos.
    
- Imágenes: fotografías.
    
- Sonidos: grabaciones.
    
- Vídeos: archivos multimedia.
    
- Registros: información de bases de datos.
    

### Diferencia entre datos e información

**Dato:** valor o representación que puede procesarse.

**Información:** datos interpretados dentro de un contexto que adquieren significado.

**Ejemplo:**

- Dato: `38`.
    
- Información: la temperatura de un procesador es de 38 °C.
    

---

## 1.5. Usuarios y procedimientos

Los **usuarios** son las personas que utilizan o administran el sistema informático.

Pueden ser:

- Usuarios finales.
    
- Técnicos informáticos.
    
- Administradores de sistemas.
    
- Administradores de seguridad.
    

Los **procedimientos** son las normas e instrucciones que establecen cómo utilizar y administrar un sistema.

Ejemplos:

- Realizar copias de seguridad.
    
- Actualizar el sistema operativo.
    
- Aplicar políticas de contraseñas.
    
- Gestionar permisos de acceso.
    

---

## 1.6. Funcionamiento básico de un sistema informático

Un sistema informático realiza cinco funciones principales:

### 1. Entrada

Consiste en capturar o introducir datos.

**Ejemplo:** escribir una contraseña mediante el teclado.

### 2. Procesamiento

Consiste en ejecutar operaciones sobre los datos siguiendo instrucciones.

**Ejemplo:** comprobar si una contraseña coincide con la información de autenticación almacenada.

### 3. Almacenamiento

Consiste en guardar datos o resultados para utilizarlos posteriormente.

Puede ser:

- **Temporal:** memoria RAM.
    
- **Persistente:** SSD, HDD.
    

### 4. Salida

Consiste en presentar resultados al usuario.

**Ejemplo:** mostrar un mensaje de acceso permitido.

### 5. Comunicación

Consiste en enviar y recibir información entre dispositivos o sistemas.

**Ejemplo:** un ordenador consulta un servidor mediante una red.

> **Para el examen:** entrada, procesamiento, almacenamiento, salida y comunicación son las cinco funciones básicas presentadas en la unidad.

---

# 2. Máquina de Von Neumann y sus componentes

## 2.1. Arquitectura de Von Neumann

La **arquitectura de Von Neumann** es un modelo de organización de computadores en el que los datos y las instrucciones de los programas se almacenan en una memoria compartida y son procesados por la CPU.

Su característica fundamental es el concepto de **programa almacenado**.

Esto significa que las instrucciones de un programa se guardan en memoria y el procesador puede recuperarlas y ejecutarlas.

### Componentes principales

1. CPU.
    
2. Unidad de Control.
    
3. Unidad Aritmético-Lógica.
    
4. Registros.
    
5. Memoria principal.
    
6. Dispositivos de entrada y salida.
    
7. Buses de comunicación.
    

---

## 2.2. CPU: Unidad Central de Procesamiento

La **CPU (Central Processing Unit)** es el procesador encargado de ejecutar las instrucciones de los programas y coordinar las operaciones de procesamiento.

En el modelo básico, contiene:

- Unidad de Control (UC).
    
- Unidad Aritmético-Lógica (ALU).
    
- Registros.
    

### Unidad de Control (UC)

La **Unidad de Control** interpreta las instrucciones y coordina su ejecución.

Funciones:

- Obtener instrucciones.
    
- Interpretar las operaciones.
    
- Generar señales de control.
    
- Coordinar los componentes implicados.
    

**Ejemplo:** cuando un programa solicita sumar dos números, la unidad de control organiza las operaciones necesarias para ejecutar la instrucción.

### Unidad Aritmético-Lógica (ALU)

La **ALU (Arithmetic Logic Unit)** realiza operaciones aritméticas y lógicas.

**Operaciones aritméticas:**

- Suma.
    
- Resta.
    
- Comparaciones numéricas.
    

**Operaciones lógicas:**

- AND.
    
- OR.
    
- NOT.
    
- Comparaciones lógicas.
    

**Ejemplo:**

`5 + 3 = 8`

La ALU puede realizar esta operación siguiendo las instrucciones ejecutadas por la CPU.

### Registros

Los **registros** son pequeñas unidades de almacenamiento de muy alta velocidad situadas dentro de la CPU.

Almacenan temporalmente:

- Datos.
    
- Direcciones.
    
- Instrucciones o información relacionada con ellas.
    
- Resultados intermedios.
    

Son mucho más pequeños que la RAM, pero ofrecen acceso muy rápido.

### Registros importantes (ampliación)

|Registro|Función|
|---|---|
|PC (Program Counter)|Identifica la dirección de la siguiente instrucción que se buscará.|
|IR (Instruction Register)|Mantiene la instrucción que se está decodificando o ejecutando, según la arquitectura.|
|Registros generales|Guardan operandos y resultados temporales.|

---

## 2.3. Memoria principal

La **memoria principal** almacena temporalmente las instrucciones y los datos que utiliza el procesador.

En los ordenadores convencionales, esta función corresponde principalmente a la memoria RAM.

### Memoria RAM

La **RAM (Random Access Memory)** es una memoria de acceso aleatorio utilizada para mantener datos e instrucciones durante la ejecución de programas.

Características:

- Es volátil.
    
- Permite operaciones de lectura y escritura.
    
- Ofrece acceso rápido.
    
- Su capacidad influye en la cantidad de información que puede mantenerse disponible en memoria.
    

**Memoria volátil:** memoria que normalmente pierde su contenido cuando deja de recibir alimentación eléctrica.

**Ejemplo:** al abrir un videojuego, parte de sus instrucciones y recursos se cargan desde el SSD a la RAM para utilizarlos durante la ejecución.

---

## 2.4. Buses del sistema

Un **bus** es un sistema de comunicación que permite intercambiar información entre componentes informáticos.

En el modelo clásico existen tres tipos principales.

### Bus de datos

Transporta los datos y las instrucciones entre los componentes.

**Ejemplo:** transferir un valor desde la memoria RAM a la CPU.

### Bus de direcciones

Identifica las posiciones de memoria o los destinos a los que se quiere acceder.

**Ejemplo:** indicar qué posición de memoria debe leerse.

### Bus de control

Transporta señales necesarias para coordinar las operaciones.

Ejemplos:

- Lectura.
    
- Escritura.
    
- Sincronización.
    
- Otras señales de control.
    

### Resumen

|Bus|¿Qué transporta?|
|---|---|
|Datos|Información e instrucciones.|
|Direcciones|Identificadores de posiciones o destinos.|
|Control|Señales de coordinación.|

---

## 2.5. Ciclo de instrucción de la CPU (ampliación)

El **ciclo de instrucción** es la secuencia de operaciones que realiza la CPU para ejecutar instrucciones.

Se puede explicar mediante tres etapas fundamentales:

### 1. Fetch (búsqueda)

La CPU obtiene la instrucción que debe ejecutar.

### 2. Decode (decodificación)

La CPU interpreta la instrucción y determina qué operación debe realizar.

### 3. Execute (ejecución)

La CPU realiza la operación indicada.

En determinadas instrucciones también intervienen accesos a memoria y escritura de resultados.

**Ejemplo práctico:**

Para ejecutar una suma:

1. La CPU obtiene la instrucción.
    
2. Interpreta que debe realizar una suma.
    
3. Obtiene los operandos necesarios.
    
4. La ALU realiza la operación.
    
5. El resultado se guarda en un registro o en memoria.
    

> **Para el examen:** la UC coordina, la ALU calcula, los registros almacenan información temporal y los buses permiten comunicar componentes.

---

# 3. La placa base y sus estándares

## 3.1. ¿Qué es una placa base?

La **placa base**, también denominada **placa madre o motherboard**, es la placa de circuito impreso principal donde se instalan e interconectan los componentes del ordenador.

Permite:

- Conectar componentes.
    
- Distribuir alimentación eléctrica.
    
- Facilitar la comunicación entre dispositivos.
    
- Incorporar puertos y conectores.
    
- Ampliar las capacidades del equipo.
    

---

## 3.2. Componentes de la placa base

### 1. Socket del procesador

El **socket** es el zócalo físico y eléctrico donde se instala la CPU.

Cada procesador necesita un socket compatible.

La compatibilidad también puede depender del chipset y de la versión de BIOS/UEFI.

**Ejemplo:** no es posible instalar cualquier procesador en cualquier placa base.

### 2. Ranuras de memoria RAM

Son los conectores donde se instalan los módulos de memoria.

En ordenadores de sobremesa suelen utilizarse módulos DIMM.

**Ejemplo:**

Dos módulos de 8 GB permiten disponer de 16 GB de RAM.

### 3. Chipset o PCH

El **chipset** es el conjunto de circuitos que gestiona determinadas funciones de comunicación y entrada/salida de la plataforma.

En muchos equipos actuales se utiliza un controlador denominado **PCH (Platform Controller Hub)**.

Funciones habituales:

- Gestionar conexiones de dispositivos.
    
- Proporcionar interfaces de entrada/salida.
    
- Facilitar la comunicación con determinados periféricos.
    

En sistemas modernos, algunas funciones que antes correspondían al chipset están integradas en la CPU.

### 4. Conectores SATA y M.2

Permiten conectar dispositivos de almacenamiento compatibles.

**SATA (Serial ATA)**

Es una interfaz de comunicación utilizada por discos duros y unidades SSD SATA.

**M.2**

Es un formato físico de conexión que puede utilizarse para unidades SSD y otros dispositivos.

**NVMe (Non-Volatile Memory Express)**

Es un protocolo diseñado para acceder a dispositivos de almacenamiento no volátil, habitualmente mediante PCIe.

**Diferencia importante:**

- SATA: interfaz de comunicación.
    
- M.2: formato de conexión.
    
- NVMe: protocolo de almacenamiento.
    

No todos los SSD M.2 utilizan NVMe.

### 5. Ranuras PCI Express

**PCIe (Peripheral Component Interconnect Express)** es una interfaz de expansión de alta velocidad.

Permite conectar:

- Tarjetas gráficas.
    
- Tarjetas de red.
    
- Controladoras de almacenamiento.
    
- Tarjetas de sonido.
    
- Otros dispositivos compatibles.
    

Las conexiones PCIe pueden disponer de distinto número de líneas, como x1, x4, x8 y x16.

### 6. BIOS/UEFI

La **BIOS (Basic Input/Output System)** es el firmware tradicional encargado de participar en la inicialización del hardware y el arranque del equipo.

**UEFI (Unified Extensible Firmware Interface)** es la interfaz de firmware moderna que sustituye al BIOS tradicional en la mayoría de ordenadores actuales.

Funciones habituales:

- Inicializar el hardware.
    
- Ejecutar comprobaciones de arranque.
    
- Permitir configurar parámetros del sistema.
    
- Iniciar el proceso de carga del sistema operativo.
    

### 7. Conectores de alimentación

Permiten que la placa base y otros componentes reciban energía de la fuente de alimentación.

Ejemplos:

- Conector ATX principal.
    
- Conector de alimentación de CPU.
    

### 8. Puertos traseros

Son las conexiones externas disponibles en la placa base.

Ejemplos:

- USB.
    
- Ethernet.
    
- Audio.
    
- HDMI o DisplayPort, cuando estén disponibles.
    
- Otros puertos según el modelo.
    

---

## 3.3. Funciones de la placa base

### Distribución de energía

Proporciona conexiones eléctricas y circuitos de regulación para alimentar distintos componentes.

### Comunicación

Permite intercambiar información entre CPU, memoria, almacenamiento y dispositivos.

### Conectividad

Ofrece conexiones internas y externas.

### Ampliación

Permite incorporar componentes compatibles, como memoria RAM o tarjetas PCIe.

---

## 3.4. Estándares físicos de placa base

El **factor de forma** es el estándar que define características físicas de una placa base, como dimensiones y disposición de determinados elementos.

### ATX

Dimensiones habituales: **305 × 244 mm**.

Características:

- Mayor superficie.
    
- Generalmente más posibilidades de expansión.
    
- Utilizado en equipos de escritorio y gaming.
    

### Micro-ATX

Dimensiones habituales: **244 × 244 mm**.

Características:

- Tamaño intermedio.
    
- Equilibrio entre expansión y espacio.
    
- Utilizado en equipos de uso general.
    

### Mini-ITX

Dimensiones: **170 × 170 mm**.

Características:

- Tamaño reducido.
    
- Menos espacio para ampliaciones.
    
- Utilizado en ordenadores compactos y equipos de bajo consumo.
    

### Comparación

|Estándar|Dimensiones|Uso habitual|
|---|---|---|
|ATX|305 × 244 mm|Sobremesa y gaming|
|Micro-ATX|244 × 244 mm|Uso general|
|Mini-ITX|170 × 170 mm|Equipos compactos|

---

## 3.5. Factores para elegir una placa base

Antes de elegir una placa base hay que comprobar:

1. **Socket:** compatibilidad con el procesador.
    
2. **RAM:** tipo, capacidad máxima y número de ranuras.
    
3. **Almacenamiento:** conexiones SATA y M.2 disponibles.
    
4. **Expansión:** número y características de las ranuras PCIe.
    
5. **Conectividad:** puertos USB, red y otras conexiones.
    
6. **Formato:** compatibilidad con la caja del ordenador.
    
7. **Firmware:** soporte de la CPU y funciones necesarias.
    

> **Para el examen:** la placa base conecta, alimenta y facilita la comunicación entre los componentes del ordenador.

---

# 4. Arquitectura Von Neumann frente a Harvard

## 4.1. ¿Qué es una arquitectura de computadores?

La **arquitectura de computadores** describe cómo se organiza un sistema informático y cómo interactúan sus componentes para ejecutar instrucciones y procesar datos.

En esta unidad se comparan dos modelos clásicos:

- Arquitectura de Von Neumann.
    
- Arquitectura Harvard.
    

La principal diferencia es cómo se organizan los accesos a instrucciones y datos.

---

## 4.2. Arquitectura de Von Neumann

La arquitectura de Von Neumann utiliza una memoria compartida para almacenar tanto instrucciones como datos.

En su modelo clásico, la CPU utiliza recursos de comunicación compartidos para acceder a ambos.

### Características

- Memoria común para datos e instrucciones.
    
- Buses compartidos en el modelo clásico.
    
- Diseño conceptual sencillo.
    
- Flexibilidad en el uso de memoria.
    
- Posibilidad de limitaciones por el acceso compartido.
    

### Ventajas

- Simplicidad.
    
- Flexibilidad.
    
- Menor complejidad en el modelo básico.
    
- Adecuada para sistemas de propósito general.
    

### Inconvenientes

- Competencia por los recursos de acceso a memoria.
    
- Posible cuello de botella.
    

### Cuello de botella de Von Neumann

Es una limitación de rendimiento que aparece cuando la transferencia de información entre CPU y memoria no puede satisfacer toda la demanda de instrucciones y datos.

**Ejemplo:**

Si la CPU necesita obtener instrucciones y datos utilizando un recurso compartido con capacidad limitada, ambos accesos pueden competir y retrasar la ejecución.

---

## 4.3. Arquitectura Harvard

La arquitectura Harvard utiliza memorias o espacios de memoria separados para instrucciones y datos.

También dispone de vías de acceso independientes.

### Características

- Separación de instrucciones y datos.
    
- Accesos independientes.
    
- Posibilidad de acceder simultáneamente a instrucciones y datos.
    
- Mayor complejidad de diseño.
    

### Ventajas

- Reduce la competencia entre determinados accesos.
    
- Puede mejorar el rendimiento.
    
- Resulta útil en sistemas especializados.
    

### Inconvenientes

- Mayor complejidad.
    
- Posible aumento del coste.
    
- Menor flexibilidad en algunos diseños.
    

### Aplicaciones habituales

- Microcontroladores.
    
- Procesadores digitales de señales (DSP).
    
- Sistemas embebidos.
    

Un **sistema embebido** es un sistema informático integrado en otro dispositivo y diseñado para realizar funciones específicas.

Ejemplos: controladores de electrodomésticos, sistemas electrónicos de vehículos y determinados dispositivos industriales.

---

## 4.4. Comparación de arquitecturas

|Característica|Von Neumann|Harvard|
|---|---|---|
|Memoria|Compartida|Separada|
|Instrucciones y datos|Mismo espacio de memoria|Espacios diferenciados|
|Buses|Compartidos en el modelo clásico|Independientes|
|Acceso simultáneo|Limitado por recursos compartidos|Puede realizarse|
|Complejidad|Menor|Mayor|
|Rendimiento|Puede sufrir cuello de botella|Puede reducir esa limitación|
|Usos habituales|Computación general|Sistemas embebidos y especializados|

### Arquitectura Harvard modificada (ampliación)

Muchos procesadores modernos combinan características de ambas arquitecturas.

Por ejemplo, pueden utilizar:

- Caché de instrucciones independiente.
    
- Caché de datos independiente.
    
- Memoria RAM principal compartida.
    

Esto permite aprovechar determinadas ventajas del acceso independiente sin necesitar memorias principales completamente separadas.

---

# 5. Conceptos adicionales importantes

## 5.1. Memoria caché

La **memoria caché** es una memoria pequeña y muy rápida que almacena temporalmente copias de datos e instrucciones que pueden necesitarse próximamente.

Su objetivo es reducir el tiempo medio de acceso a la información.

Niveles habituales:

- **L1:** pequeña y muy rápida.
    
- **L2:** normalmente mayor que L1.
    
- **L3:** normalmente de mayor capacidad y compartida entre varios núcleos en muchos procesadores.
    

La organización exacta depende de la CPU.

## 5.2. Núcleos del procesador

Un **núcleo** es una unidad de procesamiento dentro de la CPU capaz de ejecutar instrucciones.

Una CPU multinúcleo puede ejecutar trabajo en varios núcleos.

**Ejemplo:** una CPU de 8 núcleos dispone de ocho núcleos físicos de procesamiento.

## 5.3. Hilos de ejecución

Un **hilo de ejecución** es una secuencia de instrucciones planificada para ejecutarse en un procesador.

Algunos procesadores permiten que un núcleo físico mantenga varios contextos de ejecución de hardware mediante tecnologías de multithreading simultáneo.

**Importante:** un hilo lógico de hardware no equivale a un núcleo físico completo.

## 5.4. Frecuencia de la CPU

La **frecuencia** indica el número de ciclos de reloj por segundo.

Se mide en hercios (Hz).

**Ejemplo:**

3 GHz equivalen a 3.000 millones de ciclos de reloj por segundo.

No significa que el procesador ejecute exactamente 3.000 millones de instrucciones por segundo, porque cada instrucción puede requerir distintos recursos y ciclos.

---

# 6. Glosario para memorizar

|Término|Definición|
|---|---|
|Sistema informático|Conjunto de elementos que procesan información.|
|Hardware|Componentes físicos.|
|Software|Programas e instrucciones.|
|CPU|Unidad central de procesamiento.|
|UC|Unidad que coordina la ejecución de instrucciones.|
|ALU|Unidad que realiza operaciones aritméticas y lógicas.|
|Registro|Almacenamiento interno rápido de la CPU.|
|RAM|Memoria principal de trabajo, normalmente volátil.|
|Bus de datos|Transporta datos e instrucciones.|
|Bus de direcciones|Identifica posiciones o destinos.|
|Bus de control|Transporta señales de coordinación.|
|Socket|Zócalo para instalar una CPU.|
|Chipset/PCH|Circuitería de gestión de conexiones de la plataforma.|
|PCIe|Interfaz de expansión de alta velocidad.|
|SATA|Interfaz de almacenamiento.|
|M.2|Formato físico de conexión.|
|NVMe|Protocolo para almacenamiento no volátil.|
|BIOS/UEFI|Firmware relacionado con inicialización y arranque.|
|ATX|Factor de forma de placa base.|
|Caché|Memoria rápida que reduce el tiempo medio de acceso.|
|Cuello de botella|Limitación que restringe el rendimiento.|
|Von Neumann|Modelo con memoria compartida para datos e instrucciones.|
|Harvard|Modelo con memorias o accesos separados.|

---

# 7. Preguntas de repaso

1. ¿Qué es un sistema informático?
    
2. ¿Cuáles son sus cuatro elementos principales?
    
3. ¿Qué diferencia existe entre hardware y software?
    
4. ¿Qué funciones realiza un sistema operativo?
    
5. ¿Cuáles son las cinco etapas funcionales de un sistema informático?
    
6. ¿En qué consiste la arquitectura de Von Neumann?
    
7. ¿Qué función tiene la CPU?
    
8. ¿Cuál es la diferencia entre la Unidad de Control y la ALU?
    
9. ¿Para qué sirven los registros?
    
10. ¿Qué diferencia existe entre los buses de datos, direcciones y control?
    
11. ¿En qué consiste el ciclo Fetch-Decode-Execute?
    
12. ¿Qué es una placa base?
    
13. ¿Qué función tiene el socket?
    
14. ¿Para qué sirve el chipset?
    
15. ¿Qué diferencia existe entre SATA, M.2 y NVMe?
    
16. ¿Qué es PCI Express?
    
17. ¿Qué función cumple UEFI?
    
18. ¿Cuáles son las diferencias entre ATX, Micro-ATX y Mini-ITX?
    
19. ¿Qué diferencia existe entre las arquitecturas Von Neumann y Harvard?
    
20. ¿Qué es el cuello de botella de Von Neumann?
    
21. ¿Qué ventajas ofrece la arquitectura Harvard?
    
22. ¿Qué es la memoria caché y para qué sirve?
    
23. ¿Qué diferencia hay entre un núcleo físico y un procesador lógico?
    
24. ¿Por qué una frecuencia de 3 GHz no implica ejecutar 3.000 millones de instrucciones por segundo?
    

---

# 8. Resumen final para el examen

- **Sistema informático:** hardware, software, datos, usuarios y procedimientos.
    
- **Funciones básicas:** entrada, procesamiento, almacenamiento, salida y comunicación.
    
- **CPU:** ejecuta instrucciones y coordina el procesamiento.
    
- **UC:** interpreta y coordina instrucciones.
    
- **ALU:** realiza operaciones aritméticas y lógicas.
    
- **Registros:** almacenan información temporal dentro de la CPU.
    
- **RAM:** mantiene temporalmente instrucciones y datos en uso.
    
- **Bus de datos:** transporta información.
    
- **Bus de direcciones:** identifica posiciones o destinos.
    
- **Bus de control:** coordina operaciones mediante señales.
    
- **Placa base:** conecta y permite comunicar los componentes.
    
- **Socket:** determina parte de la compatibilidad de la CPU.
    
- **Chipset/PCH:** gestiona determinadas conexiones y funciones de entrada/salida.
    
- **PCIe:** interfaz de expansión.
    
- **SATA:** interfaz utilizada por unidades de almacenamiento.
    
- **M.2:** formato de conexión.
    
- **NVMe:** protocolo de almacenamiento.
    
- **BIOS/UEFI:** firmware relacionado con inicialización y arranque.
    
- **ATX, Micro-ATX y Mini-ITX:** factores de forma de placas base.
    
- **Von Neumann:** memoria compartida para instrucciones y datos.
    
- **Harvard:** memorias o vías de acceso independientes.
    
- **Cuello de botella:** limitación de rendimiento provocada por un recurso compartido.