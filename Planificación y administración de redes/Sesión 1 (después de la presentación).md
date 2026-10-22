## 1. Hardware (HW)

**Definición:** el **hardware** es el conjunto de componentes físicos de un equipo informático, es decir, las piezas que podemos tocar: procesador, RAM, placa base, almacenamiento, etc.

**Función:** proporcionar los recursos necesarios para que se ejecuten los programas (**software**). Una buena elección de componentes permite un trabajo eficiente y un rendimiento adecuado a las necesidades.

**Ejemplo:** para ejecutar varias máquinas virtuales conviene contar con suficiente RAM, núcleos de CPU y espacio de almacenamiento.

## 2. Procesador (CPU)

**Definición:** la **CPU** (_Central Processing Unit_, unidad central de procesamiento) es el componente encargado de **interpretar y ejecutar instrucciones de los programas y realizar operaciones aritméticas y lógicas**. Se suele llamar «cerebro del ordenador».

### Características principales

- **Núcleo (_core_):** unidad de ejecución dentro de la CPU capaz de procesar instrucciones. Varios núcleos permiten ejecutar trabajo en paralelo.
- **Subproceso o hilo (_thread_):** secuencia de instrucciones que un programa puede ejecutar. Algunas CPU pueden manejar más de un hilo de hardware por núcleo mediante tecnologías como _Hyper-Threading_ (Intel) o SMT. **No es lo mismo un hilo que un núcleo físico**.
- **Frecuencia de reloj:** número de ciclos de reloj por segundo; se expresa en **Hz**, normalmente **GHz**. Por ejemplo, 3 GHz equivale a 3.000 millones de ciclos por segundo. **Más GHz no implica siempre mayor rendimiento**: también influyen la arquitectura, el trabajo por ciclo y los núcleos.
- **Memoria caché:** memoria pequeña y muy rápida, integrada en la CPU, que conserva copias de datos e instrucciones usados frecuentemente para reducir accesos más lentos a la RAM. Puede organizarse en niveles **L1, L2 y L3** (aclaración adicional).
- **TDP (_Thermal Design Power_, potencia de diseño térmico):** valor de referencia térmica, normalmente expresado en **W**, que ayuda a dimensionar la refrigeración. **No equivale necesariamente al consumo eléctrico máximo real de la CPU**.

**Ejemplo:** una CPU de 8 núcleos y 16 hilos puede atender múltiples trabajos, como un navegador, un IDE y máquinas virtuales, pero su rendimiento depende de la carga concreta.

> [!important] Para el examen  
> CPU = ejecución de instrucciones; núcleos = unidades de procesamiento; frecuencia = ciclos/s; caché = acceso rápido a datos frecuentes; TDP = referencia para refrigeración.

## 3. Memoria RAM

**Definición:** la **RAM** (_Random Access Memory_, memoria de acceso aleatorio) es la **memoria principal y volátil** del ordenador. Almacena temporalmente los datos y programas que están en uso para que la CPU pueda acceder a ellos rápidamente.

**Volátil** significa que su contenido se pierde cuando deja de recibir alimentación eléctrica.

**Funciones y características:**

- Facilita la ejecución simultánea de programas (**multitarea**).
- Una capacidad suficiente evita recurrir excesivamente al almacenamiento como memoria auxiliar, lo que puede ralentizar el equipo.
- Su capacidad se expresa en **GB** (también MB o TB).
- **Tener más RAM no acelera automáticamente todo:** resulta útil cuando las aplicaciones necesitan esa capacidad.

**Ejemplo:** 16 GB pueden ser suficientes para muchos usos cotidianos, pero ejecutar varias máquinas virtuales o editar vídeo de alta resolución puede requerir más. No existe una cifra universal válida para todos los equipos.

**Diferencia fundamental:** la RAM guarda datos **temporalmente**; un SSD o HDD los conserva **aunque apaguemos el ordenador**.

## 4. Tarjeta gráfica (GPU)

**Definición:** la **tarjeta gráfica** es el componente encargado de procesar información visual y generar imágenes que se muestran en pantalla. Su unidad de cálculo principal es la **GPU** (_Graphics Processing Unit_, unidad de procesamiento gráfico).

**Funciones del material:**

- **Renderización gráfica:** generar imágenes, gráficos 2D y 3D, vídeo y animaciones.
- **Procesamiento de texturas:** aplicar detalles visuales a superficies de objetos 3D.
- **Cálculos geométricos:** determinar posiciones, formas y transformaciones de objetos.
- **Procesamiento de píxeles:** aplicar colores, sombras y efectos a la imagen.
- **Cálculos de IA y otras disciplinas:** determinadas GPU aceleran operaciones paralelas en aprendizaje automático, ingeniería y simulaciones.

**Características para elegir una gráfica:**

- **Rendimiento de la GPU:** capacidad de cálculo gráfico.
- **VRAM (_Video RAM_):** memoria utilizada por la GPU para almacenar texturas y otros datos de trabajo gráfico.
- **Puertos de salida:** conexiones para monitores, por ejemplo HDMI o DisplayPort (ejemplos añadidos).

**Aclaración:** puede existir una GPU **integrada** en el procesador o una tarjeta gráfica **dedicada**.

## 5. Almacenamiento: SSD y HDD

**Definición:** el **almacenamiento** es el conjunto de dispositivos que permiten **guardar de forma persistente** archivos, programas y el sistema operativo.

|Característica|SSD|HDD|
|---|---|---|
|Tecnología|Memoria flash|Platos magnéticos y mecanismo de lectura|
|Partes móviles|No|Sí|
|Velocidad habitual|Mayor|Menor|
|Uso frecuente|Sistema operativo, programas y trabajo rápido|Archivos voluminosos y copias de seguridad|

- **SSD (_Solid-State Drive_):** unidad de estado sólido; suele mejorar la rapidez de arranque y carga de aplicaciones.
- **HDD (_Hard Disk Drive_):** disco duro mecánico; utiliza componentes móviles para leer y escribir datos.
- **Capacidad:** se expresa en **GB** y **TB**.

**Ejemplo:** instalar el sistema operativo en un SSD y guardar archivos grandes en un HDD es una configuración posible, no obligatoria.

> [!tip] No confundir  
> La **RAM** es memoria de trabajo volátil; **SSD/HDD** son almacenamiento persistente.

## 6. Fuente de alimentación (PSU)

**Definición:** la **fuente de alimentación** o **PSU** (_Power Supply Unit_) es el componente que **suministra energía eléctrica a las piezas internas** del ordenador. En un PC convencional convierte la corriente alterna de la red en tensiones continuas adecuadas para los componentes (aclaración adicional).

### Características

1. **Voltaje o tensión de salida (V):** diferencia de potencial eléctrico que debe ajustarse a las especificaciones del componente.
2. **Corriente de salida (A):** cantidad de carga eléctrica que circula por unidad de tiempo; la fuente debe poder suministrar la corriente requerida.
3. **Eficiencia energética:** proporción entre la energía útil entregada y la consumida; parte de la energía se pierde, principalmente como calor.
4. **Conectores y cables:** proporcionan alimentación a placa base, GPU y unidades de almacenamiento.
5. **Protecciones:** mecanismos frente a sobrecorriente, sobretensión y cortocircuitos, entre otros riesgos.

**Concepto complementario:** la potencia eléctrica se mide en **vatios (W)**; en corriente continua, **P = V × I**.

**Ejemplo:** una GPU potente puede requerir una fuente de mayor potencia y conectores compatibles.

## 7. Placa base (_motherboard_)

**Definición:** la **placa base** o **placa madre** es la **tarjeta de circuito principal** que conecta los componentes del equipo y permite que se comuniquen entre sí.

**Determina la compatibilidad y posibilidades de ampliación**, entre otras cosas:

- **Procesador:** zócalo (_socket_) y compatibilidad de plataforma.
- **Memoria RAM:** tipo, número de ranuras y capacidad admitida.
- **Tarjetas de expansión:** ranuras disponibles, como PCIe.
- **Almacenamiento y periféricos:** conexiones y puertos disponibles.

**Ejemplo:** no basta con comprar cualquier procesador: debe ser compatible con la placa base.

## 8. Refrigeración

**Definición:** la **refrigeración** es el conjunto de elementos que **extraen y disipan el calor** generado por los componentes para mantener temperaturas de funcionamiento seguras.

### Tipos y elementos

- **Ventiladores:** mueven el aire para ayudar a introducir aire fresco y expulsar aire caliente de la caja.
- **Disipadores de calor:** piezas metálicas que absorben y reparten el calor en una superficie mayor para facilitar su transferencia al aire. Pueden funcionar con ventiladores.
- **Refrigeración líquida:** sistema que transporta calor mediante un líquido hasta un radiador, donde se disipa, habitualmente con ayuda de ventiladores.
- **Pasta térmica:** material aplicado entre CPU y disipador que **rellena irregularidades microscópicas** y mejora el contacto térmico; **no sustituye al disipador**.

**¿Por qué es importante?** Si un procesador se calienta demasiado, puede reducir automáticamente su rendimiento para protegerse (_thermal throttling_, aclaración adicional).

**Aclaración:** la refrigeración líquida no es siempre superior a cualquier sistema por aire; depende del diseño y la capacidad del sistema.

## 9. Periféricos

**Definición:** los **periféricos** son dispositivos que se conectan al equipo para **introducir información, mostrar resultados o ampliar sus funciones**.

**Clasificación orientativa (ampliación):**

- **Entrada:** teclado, ratón, tableta gráfica.
- **Salida:** monitor, altavoces.
- **Entrada y salida / comunicación:** tarjeta de red y otros dispositivos que envían y reciben información.

**Ejemplos del material:** monitor, tableta gráfica, superficies de control, tarjetas de sonido, tarjetas de red, teclados especializados y ratón _trackball_.

## 10. Repaso rápido para examen

|Componente|Definición que debes recordar|
|---|---|
|CPU|Ejecuta instrucciones y realiza operaciones.|
|Caché|Memoria rápida de la CPU para datos e instrucciones frecuentes.|
|RAM|Memoria principal temporal y volátil.|
|GPU|Procesa gráficos y determinados cálculos paralelos.|
|SSD|Almacenamiento persistente basado en memoria flash.|
|HDD|Almacenamiento persistente con componentes mecánicos.|
|PSU|Suministra la energía eléctrica adecuada al equipo.|
|Placa base|Conecta componentes y condiciona su compatibilidad.|
|Refrigeración|Extrae y disipa calor.|
|Pasta térmica|Mejora la transferencia térmica entre chip y disipador.|
|Periféricos|Permiten interacción y ampliación de funciones.|

### Preguntas de autoevaluación

1. ¿En qué se diferencia un núcleo físico de un hilo de ejecución?
2. ¿Por qué más GHz no garantiza siempre una CPU más rápida?
3. ¿Por qué se pierde el contenido de la RAM al apagar el equipo?
4. ¿Qué diferencia principal hay entre SSD y HDD?
5. ¿Para qué sirve la VRAM?
6. ¿Qué mide el TDP y por qué importa?
7. ¿Qué compatibilidades determina la placa base?
8. ¿Qué función tiene la pasta térmica?
9. ¿Qué protecciones debe incorporar una fuente de alimentación?
10. ¿Qué periférico permite la comunicación con una red?