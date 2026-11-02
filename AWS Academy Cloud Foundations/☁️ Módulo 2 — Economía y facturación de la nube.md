# 1. Modelo de precios de AWS

AWS utiliza principalmente el modelo de **pago por uso**, es decir, pagamos por los recursos que consumimos.

## 1.1. ¿Cómo se paga por AWS?

Existen tres principios principales:

1. **Pagar por lo que utilizas:** Solo pagas por los servicios consumidos.
    
2. **Pagar menos al reservar:** Puedes obtener descuentos al comprometerte a utilizar determinados recursos.
    
3. **Pagar menos cuanto más utilizas:** Algunos servicios ofrecen descuentos por volumen.
    

### Tres factores principales del coste

|Factor|Explicación|
|---|---|
|Computación|Se cobra según los recursos y el tiempo de uso.|
|Almacenamiento|Normalmente se cobra por GB almacenado.|
|Transferencia de datos|Generalmente se cobra por los datos que salen de AWS.|

> [!IMPORTANT]  
> Normalmente, la transferencia de datos hacia AWS es gratuita, mientras que la salida de datos puede generar costes.

## 1.2. Pagar por lo que utilizas

En un centro de datos tradicional, una empresa debe comprar servidores y mantenerlos aunque no los utilice.

En AWS:

- No necesitas comprar servidores físicos.
    
- Pagas según el consumo.
    
- Puedes aumentar o reducir los recursos cuando los necesites.
    

**Ejemplo:** Si necesitas un servidor durante 5 horas, puedes pagar únicamente por esas 5 horas, según las condiciones del servicio.

## 1.3. Pagar menos si utilizas más

AWS ofrece descuentos por volumen en determinados servicios.

Por ejemplo:

- Amazon S3: almacenamiento de objetos.
    
- Amazon EBS: almacenamiento en bloques.
    
- Amazon EFS: almacenamiento de archivos.
    

En algunos servicios, **el precio por GB disminuye al aumentar el volumen utilizado**.

## 1.4. Pagar menos a medida que AWS crece

AWS aprovecha las **economías de escala**.

Esto significa que, al operar una infraestructura muy grande, puede reducir sus costes y trasladar parte de esos ahorros a sus clientes.

## 1.5. Precios personalizados

AWS puede ofrecer acuerdos de precios personalizados a empresas con grandes necesidades de infraestructura o consumo.

## Instancias reservadas (Reserved Instances)

Permiten obtener descuentos al comprometerse a utilizar determinados recursos de AWS durante **1 o 3 años**.

Existen tres modalidades de pago:

|Modalidad|Significado|
|---|---|
|AURI|Pagas todo por adelantado.|
|PURI|Pagas una parte al principio y el resto periódicamente.|
|NURI|No pagas inicialmente; realizas pagos periódicos.|

> [!IMPORTANT]  
> Para el examen, recuerda: **AURI, PURI y NURI**.
## 1.6. Capa gratuita de AWS

La **AWS Free Tier** permite utilizar determinados servicios gratuitamente dentro de unos límites.

Existen ofertas gratuitas que pueden depender del tiempo, del servicio o del consumo.

> [!WARNING]  
> La capa gratuita no significa que todos los servicios sean gratuitos. Superar los límites puede generar cargos. Las condiciones actuales pueden diferir de las mostradas en el curso.

### Servicios que pueden utilizarse sin cargos propios

|Servicio|Función|
|---|---|
|Amazon VPC|Crear redes virtuales privadas.|
|AWS IAM|Administrar usuarios y permisos.|
|AWS CloudFormation|Automatizar la creación de infraestructura.|
|AWS Auto Scaling|Ajustar automáticamente los recursos.|
|AWS Elastic Beanstalk|Facilitar el despliegue de aplicaciones.|

**Importante:** Algunos de estos servicios no tienen un cargo adicional por su función principal, pero los recursos asociados sí pueden generar costes.

---

# 2. Coste total de propiedad (TCO)

## 2.1. ¿Qué es el TCO?

**TCO (Total Cost of Ownership)** significa _coste total de propiedad_.

Es el cálculo de todos los costes directos e indirectos necesarios para mantener una infraestructura informática.

Sirve para comparar el coste de tener servidores propios con el de utilizar AWS.

### Infraestructura tradicional frente a AWS

|Infraestructura tradicional|AWS|
|---|---|
|Comprar servidores|Utilizar recursos bajo demanda|
|Gastos iniciales elevados|Menor inversión inicial|
|Mantener instalaciones|Infraestructura gestionada por AWS|
|Comprar capacidad adicional|Escalar según las necesidades|
|Mantener hardware propio|AWS mantiene la infraestructura física|

## 2.2. Costes que considera el TCO

Los principales costes son:

1. **Servidores:** Hardware, software y mantenimiento.
    
2. **Almacenamiento:** Discos y sistemas de almacenamiento.
    
3. **Redes:** Equipos de red y comunicaciones.
    
4. **Personal de TI:** Administración y mantenimiento.
    
5. **Instalaciones:** Electricidad, espacio y refrigeración.
    

## 2.3. Calculadora de precios de AWS

**AWS Pricing Calculator** permite estimar cuánto costará utilizar determinados servicios de AWS.

Se utiliza para:

- Calcular costes mensuales estimados.
    
- Comparar diferentes configuraciones.
    
- Planificar presupuestos.
    
- Identificar posibles ahorros.
    

> [!IMPORTANT]  
> **TCO:** Compara el coste total de diferentes infraestructuras.
> 
> **AWS Pricing Calculator:** Estima cuánto costará utilizar servicios de AWS.

---

# 3. AWS Organizations

## 3.1. ¿Qué es AWS Organizations?

**AWS Organizations** es un servicio que permite administrar varias cuentas de AWS desde una organización central.

Sus principales funciones son:

- Administrar múltiples cuentas.
    
- Centralizar la facturación.
    
- Organizar las cuentas por departamentos.
    
- Aplicar políticas de control.
    

**Ejemplo:** Una empresa puede tener cuentas independientes para desarrollo, producción y seguridad.

## 3.2. Terminología de AWS Organizations

|Concepto|Significado|
|---|---|
|Organización|Conjunto de cuentas de AWS administradas conjuntamente.|
|Cuenta de administración|Cuenta principal desde la que se administra la organización.|
|Raíz (Root)|Nivel superior de la estructura de la organización.|
|OU|Unidad organizativa que agrupa cuentas u otras OU.|
|SCP|Política que establece límites sobre los permisos disponibles.|

### Ejemplo de estructura

```
Organización
│
└── Raíz
    │
    ├── OU Desarrollo
    │   ├── Cuenta 1
    │   └── Cuenta 2
    │
    └── OU Producción
        ├── Cuenta 3
        └── Cuenta 4
```

## 3.3. Características y beneficios

- **Administración centralizada:** Gestionar varias cuentas.
    
- **Facturación consolidada:** Reunir los gastos de diferentes cuentas.
    
- **Seguridad:** Aplicar restricciones mediante políticas.
    
- **Organización:** Separar departamentos y entornos.
    

## 3.4. Seguridad con AWS Organizations

Existen dos conceptos importantes:

### AWS IAM

Permite administrar los permisos de usuarios, grupos y roles.

**Ejemplo:** Permitir que un usuario consulte Amazon S3.

### Service Control Policies (SCP)

Establecen los permisos máximos disponibles para las cuentas de una organización.

**Ejemplo:** Impedir que determinadas cuentas utilicen ciertos servicios.

> [!IMPORTANT]  
> **IAM:** Gestiona los permisos de acceso.
> 
> **SCP:** Limita los permisos máximos disponibles, pero no concede permisos por sí misma.

## 3.5. Configuración de AWS Organizations

Pasos básicos:

1. Crear una organización.
    
2. Crear unidades organizativas (OU).
    
3. Incorporar las cuentas correspondientes.
    
4. Crear y aplicar políticas SCP.
    
5. Comprobar que las restricciones funcionan.
    

## 3.6. Acceso a AWS Organizations

Se puede administrar mediante:

- **AWS Management Console:** Interfaz gráfica.
    
- **AWS CLI:** Línea de comandos.
    
- **AWS SDK:** Herramientas para desarrolladores.
    
- **AWS API:** Acceso mediante programación.
    

---

# 4. Herramientas de facturación de AWS

AWS proporciona herramientas para consultar, analizar y controlar los gastos.

## 4.1. Panel de facturación de AWS

**AWS Billing Dashboard** muestra un resumen general de los costes.

Permite:

- Consultar los gastos actuales.
    
- Visualizar costes por servicio.
    
- Revisar información de facturación.
    

## 4.2. Facturas mensuales (Bills)

Permite consultar las facturas y los cargos de cada mes.

Incluye:

- Coste total mensual.
    
- Gastos por servicio.
    
- Cargos adicionales.
    
- Suscripciones.
    

## 4.3. AWS Cost Explorer

Herramienta que permite **analizar los gastos mediante gráficos**.

Sirve para:

- Consultar gastos anteriores.
    
- Identificar servicios costosos.
    
- Comparar costes entre meses.
    
- Realizar previsiones de gasto.
    

## 4.4. AWS Budgets

Permite establecer presupuestos y recibir alertas.

**Ejemplo:**

Una empresa establece un presupuesto mensual de 100 €.

Puede configurar una alerta cuando el gasto alcance los 80 €.

Así puede controlar sus gastos antes de superar el presupuesto.

> [!NOTE]  
> AWS Budgets permite configurar alertas, pero estas no detienen automáticamente los servicios.

## 4.5. AWS Cost and Usage Reports

Los **informes de uso y costes** ofrecen información detallada sobre el consumo de AWS.

Permiten consultar:

- Servicios utilizados.
    
- Cantidad de recursos consumidos.
    
- Costes asociados.
    
- Información detallada de facturación.
    

### Resumen de herramientas

|Herramienta|Función|
|---|---|
|Billing Dashboard|Ver resumen de gastos.|
|Bills|Consultar facturas mensuales.|
|Cost Explorer|Analizar gastos mediante gráficos.|
|AWS Budgets|Crear presupuestos y alertas.|
|Cost and Usage Reports|Obtener informes detallados.|

---

# 5. Soporte técnico de AWS

## 5.1. AWS Support

**AWS Support** proporciona asistencia técnica para ayudar a los clientes a utilizar los servicios de AWS.

Puede utilizarse tanto para aprender como para administrar aplicaciones en producción.

### Servicios relacionados

**Technical Account Manager (TAM)**

- Proporciona asesoramiento técnico personalizado.
    
- Ayuda a planificar y mejorar el uso de AWS.
    

**AWS Trusted Advisor**

- Analiza recursos de AWS.
    
- Recomienda mejoras de seguridad, rendimiento y costes.
    

**AWS Support Concierge**

- Proporciona asistencia sobre cuentas y facturación a clientes con planes que incluyen este servicio.
    

## 5.2. Planes de soporte

El material del curso presenta cuatro planes tradicionales:

|Plan|Características|
|---|---|
|Basic|Soporte gratuito y documentación.|
|Developer|Asistencia para desarrollo y pruebas.|
|Business|Soporte 24/7 para aplicaciones en producción.|
|Enterprise|Soporte avanzado para sistemas críticos.|

### Basic Support

- Gratuito.
    
- Documentación y preguntas frecuentes.
    
- Información sobre el estado de los servicios.
    
- Sin soporte técnico para incidencias de aplicaciones.
    

### Developer Support

- Orientado al desarrollo y las pruebas.
    
- Asistencia técnica en horario comercial.
    

### Business Support

- Orientado a aplicaciones en producción.
    
- Asistencia técnica 24/7.
    
- Tiempos de respuesta más rápidos.
    

### Enterprise Support

- Orientado a sistemas críticos.
    
- Asistencia técnica 24/7.
    
- Atención especializada y orientación proactiva.
    

> [!NOTE]  
> Estos son los planes tradicionales explicados en AWS Academy. La oferta comercial de AWS Support ha evolucionado y puede incluir planes diferentes.

## 5.3. Gravedad de los casos y tiempos de respuesta

Según las diapositivas del curso:

|Gravedad|Developer|Business|Enterprise|
|---|---|---|---|
|Crítica|—|—|15 minutos|
|Urgente|—|1 hora|1 hora|
|Alta|—|4 horas|4 horas|
|Normal|12 horas|12 horas|12 horas|
|Baja|24 horas|24 horas|24 horas|

**Conceptos importantes:**

- Los casos críticos reciben mayor prioridad.
    
- Los planes superiores ofrecen tiempos de respuesta más rápidos.
    
- Enterprise ofrece el menor tiempo de respuesta para problemas críticos.
    

Los tiempos indicados corresponden al material del curso y no necesariamente a los planes vigentes.

---

# 📚 Resumen general del módulo 2

|Concepto|Qué debes recordar|
|---|---|
|Pago por uso|Pagas por los recursos consumidos.|
|Economías de escala|AWS puede reducir costes gracias a su tamaño.|
|AWS Free Tier|Permite utilizar ciertos servicios gratuitamente dentro de límites.|
|TCO|Calcula el coste total de una infraestructura.|
|AWS Pricing Calculator|Estima los costes de los servicios.|
|AWS Organizations|Administra múltiples cuentas de AWS.|
|OU|Agrupa cuentas dentro de una organización.|
|IAM|Administra permisos de acceso.|
|SCP|Establece límites máximos de permisos.|
|Billing Dashboard|Muestra un resumen de los gastos.|
|Cost Explorer|Analiza costes.|
|AWS Budgets|Establece presupuestos y alertas.|
|Cost and Usage Reports|Proporciona información detallada del consumo.|
|AWS Support|Ofrece asistencia técnica.|
|Trusted Advisor|Recomienda mejoras para los recursos.|
|TAM|Proporciona asesoramiento técnico personalizado.|

---

# 🎯 Claves para el examen AWS Cloud Foundations

Recuerda especialmente estas diferencias:

**1. ¿Quieres estimar cuánto costará utilizar AWS?**

→ AWS Pricing Calculator.

**2. ¿Quieres comparar el coste de servidores propios con AWS?**

→ TCO.

**3. ¿Quieres administrar varias cuentas de AWS?**

→ AWS Organizations.

**4. ¿Quieres limitar los permisos máximos de las cuentas?**

→ SCP.

**5. ¿Quieres analizar los gastos de meses anteriores?**

→ AWS Cost Explorer.

**6. ¿Quieres recibir una alerta cuando alcances un presupuesto?**

→ AWS Budgets.

**7. ¿Quieres consultar una factura mensual?**

→ AWS Bills.

**8. ¿Quieres recibir recomendaciones para optimizar tus recursos?**

→ AWS Trusted Advisor.

**9. ¿Quieres asesoramiento técnico personalizado?**

→ Technical Account Manager (TAM).

**10. ¿Cuál es la principal ventaja económica de AWS?**

→ Pagar por los recursos que utilizas sin tener que comprar y mantener toda la infraestructura física.

---

**Fin del módulo 2 — Economía y facturación de la nube.**

# Ampliación del módulo 2: Economía y facturación de la nube

## AWS Pricing Calculator

AWS Pricing Calculator permite calcular los costes estimados de utilizar los servicios de AWS antes de implementarlos.

### Funciones principales

- **Calcular costes mensuales:** Estimar cuánto costará utilizar determinados servicios.
    
- **Identificar oportunidades de ahorro:** Comparar configuraciones para reducir gastos.
    
- **Modelar soluciones:** Diseñar y estimar una infraestructura antes de construirla.
    
- **Explorar precios:** Consultar los cálculos y los componentes que forman una estimación.
    
- **Comparar instancias:** Seleccionar tipos de instancia según las necesidades.
    
- **Evaluar condiciones contractuales:** Comparar distintas opciones de contratación y sus costes.
    

> [!IMPORTANT]  
> AWS Pricing Calculator sirve para estimar costes antes de implementar los servicios, no para consultar las facturas reales.

---

## AWS Billing and Cost Management

AWS Billing and Cost Management es el conjunto de herramientas que permite administrar los gastos de AWS.

### Funciones principales

1. **Acceder:** Consultar información sobre costes y consumo.
    
2. **Comprender:** Identificar qué servicios generan gastos.
    
3. **Asignar:** Distribuir costes entre cuentas, departamentos o proyectos.
    
4. **Controlar:** Establecer presupuestos y alertas.
    
5. **Optimizar:** Detectar oportunidades para reducir costes.
    

### Herramientas principales

|Herramienta|Función|
|---|---|
|AWS Bills|Consultar las facturas mensuales.|
|AWS Cost Explorer|Analizar y visualizar los gastos.|
|AWS Budgets|Establecer presupuestos y alertas.|
|AWS Cost and Usage Reports|Obtener información detallada sobre costes y consumo.|

---

## AWS Trusted Advisor

AWS Trusted Advisor analiza el entorno de AWS y proporciona recomendaciones para mejorar su funcionamiento.

### Áreas de optimización

- **Seguridad:** Identificar configuraciones que pueden representar riesgos.
    
- **Costes:** Detectar oportunidades de ahorro.
    
- **Rendimiento:** Recomendar mejoras de rendimiento.
    
- **Tolerancia a errores:** Identificar posibles problemas de disponibilidad.
    
- **Límites de servicio:** Detectar recursos que se acercan a determinadas cuotas.
    

> [!IMPORTANT]  
> Si en el examen aparece una pregunta sobre qué servicio proporciona **recomendaciones para optimizar la seguridad de la infraestructura**, la respuesta es **AWS Trusted Advisor**.

---

## Pregunta de examen oficial

**¿Qué servicio de AWS proporciona recomendaciones de optimización de la seguridad de la infraestructura?**

A) API de listas de precios de AWS.

B) Instancias reservadas.

C) AWS Trusted Advisor.

D) Flota de instancias de spot de Amazon EC2.

**Respuesta correcta: C) AWS Trusted Advisor.**

**Explicación:** AWS Trusted Advisor proporciona recomendaciones para mejorar diferentes aspectos de la infraestructura, incluida la seguridad.

La palabra clave es **«recomendaciones»**.