## 1. ¿Qué es Cloud Computing?

El **Cloud Computing (computación en la nube)** permite utilizar recursos informáticos a través de Internet sin necesidad de tener servidores físicos propios.

Estos recursos pueden ser:

- Servidores.
    
- Almacenamiento.
    
- Bases de datos.
    
- Redes.
    
- Aplicaciones.
    

**Ejemplo:** En lugar de comprar un servidor para alojar una página web, puedes alquilar uno en AWS.

### Infraestructura tradicional vs. nube

|Infraestructura tradicional|Cloud Computing|
|---|---|
|Compras servidores físicos|Alquilas recursos|
|Tú mantienes los equipos|AWS mantiene la infraestructura física|
|Inversión inicial elevada|Pago según consumo|
|Ampliación más lenta|Recursos escalables|

Un **NAS doméstico** es un ejemplo de almacenamiento privado. Amazon S3 permite almacenar archivos en la nube, aunque funciona de manera diferente a un NAS.

---

## 2. Modelos de servicio: IaaS, PaaS y SaaS

Existen tres modelos principales:

|Modelo|Definición|Ejemplo|
|---|---|---|
|**IaaS**|Alquilas infraestructura, como servidores virtuales|Amazon EC2|
|**PaaS**|Plataforma para desarrollar aplicaciones sin administrar directamente los servidores|AWS Elastic Beanstalk|
|**SaaS**|Aplicaciones listas para utilizar|Gmail|

### Diferencia principal

- **IaaS:** Administras el sistema operativo y las aplicaciones.
    
- **PaaS:** Te centras principalmente en desarrollar y gestionar tus aplicaciones.
    
- **SaaS:** Simplemente utilizas el software.
    

> [!IMPORTANT]  
> **IaaS = Infraestructura**
> 
> **PaaS = Plataforma**
> 
> **SaaS = Software**

---

## 3. Ventajas de la computación en la nube

AWS destaca **6 ventajas principales**.

### 1. Cambiar CAPEX por OPEX

- **CAPEX:** Inversión inicial en infraestructura, como comprar servidores.
    
- **OPEX:** Gastos operativos, como pagar mensualmente por recursos utilizados.
    

La nube permite reducir las grandes inversiones iniciales.

### 2. Economías de escala masivas

AWS puede ofrecer precios competitivos porque compra y administra enormes cantidades de infraestructura.

### 3. Evitar estimaciones de capacidad

No necesitas comprar servidores pensando en cuántos usuarios tendrás en el futuro.

Puedes aumentar o reducir los recursos según la demanda.

### 4. Mayor velocidad y agilidad

Puedes crear servidores y otros recursos en minutos.

### 5. Reducir el mantenimiento de centros de datos

AWS se encarga de mantener la infraestructura física.

### 6. Alcance mundial en minutos

Puedes desplegar aplicaciones en diferentes regiones del mundo rápidamente.

> [!IMPORTANT]  
> Las ventajas fundamentales son **ahorro de inversión inicial, escalabilidad, rapidez y alcance mundial**.

---

## 4. ¿Qué es Amazon Web Services (AWS)?

**Amazon Web Services (AWS)** es una plataforma de servicios de computación en la nube.

Permite acceder a recursos informáticos bajo demanda.

### Características principales

- **Pago por uso:** Pagas por los recursos consumidos, según las condiciones de cada servicio.
    
- **Flexibilidad:** Puedes elegir los servicios que necesitas.
    
- **Escalabilidad:** Puedes aumentar o reducir recursos.
    
- **Disponibilidad global:** AWS dispone de infraestructura en diferentes regiones.
    
- **Integración:** Sus servicios pueden trabajar conjuntamente.
    

**Ejemplo:** Una aplicación puede utilizar EC2 como servidor, RDS como base de datos y S3 para almacenar imágenes.

---

## 5. Categorías de servicios de AWS

AWS ofrece numerosas categorías de servicios.

|Categoría|Función|
|---|---|
|Computación|Ejecutar servidores y aplicaciones|
|Almacenamiento|Guardar archivos y datos|
|Bases de datos|Almacenar y consultar información|
|Redes|Conectar recursos y distribuir contenido|
|Seguridad|Proteger sistemas y controlar accesos|
|Administración|Supervisar y gestionar recursos|
|Costes|Controlar gastos|
|Inteligencia artificial|Crear soluciones basadas en IA|
|Análisis|Analizar grandes cantidades de datos|
|IoT|Conectar dispositivos a Internet|
|Desarrollo|Crear y desplegar aplicaciones|
|Integración|Conectar aplicaciones y servicios|

También existen categorías especializadas, como realidad virtual, robótica, videojuegos y blockchain.

---

## 6. Principales servicios de AWS

### Computación

|Servicio|Función|
|---|---|
|**EC2**|Servidores virtuales|
|**Lambda**|Ejecutar código sin administrar servidores|
|**Elastic Beanstalk**|Desplegar aplicaciones|
|**EC2 Auto Scaling**|Ajustar automáticamente la cantidad de instancias EC2|
|**ECS**|Administrar contenedores|
|**EKS**|Administrar Kubernetes|
|**ECR**|Almacenar imágenes de contenedores|
|**Fargate**|Ejecutar contenedores sin gestionar servidores|

### Almacenamiento

|Servicio|Función|
|---|---|
|**S3**|Almacenamiento de objetos|
|**S3 Glacier**|Almacenamiento para archivos de acceso poco frecuente|
|**EBS**|Discos para instancias EC2|
|**EFS**|Sistema de archivos compartido|

### Bases de datos

|Servicio|Función|
|---|---|
|**RDS**|Bases de datos relacionales|
|**DynamoDB**|Base de datos NoSQL|
|**Aurora**|Base de datos relacional administrada|
|**Redshift**|Análisis de grandes volúmenes de datos|

### Redes

|Servicio|Función|
|---|---|
|**VPC**|Crear redes virtuales|
|**Route 53**|Servicio DNS|
|**CloudFront**|Distribuir contenido rápidamente|
|**Elastic Load Balancing**|Repartir tráfico entre recursos|

### Seguridad

|Servicio|Función|
|---|---|
|**IAM**|Gestionar usuarios, roles y permisos|
|**Cognito**|Autenticación de usuarios de aplicaciones|
|**Shield**|Protección contra ataques DDoS|
|**Artifact**|Acceso a documentación de cumplimiento|
|**KMS**|Administrar claves de cifrado|

### Administración y costes

|Servicio|Función|
|---|---|
|**CloudWatch**|Monitorizar recursos|
|**CloudTrail**|Registrar actividades y llamadas a API|
|**Trusted Advisor**|Recomendar mejoras|
|**AWS Config**|Evaluar configuraciones de recursos|
|**AWS Organizations**|Administrar varias cuentas|
|**AWS CLI**|Gestionar AWS mediante comandos|
|**AWS Management Console**|Administrar AWS desde el navegador|
|**AWS Auto Scaling**|Ajustar automáticamente recursos compatibles|
|**Well-Architected Tool**|Revisar arquitecturas según buenas prácticas|
|**AWS Budgets**|Establecer presupuestos y alertas|
|**Cost Explorer**|Analizar gastos|
|**Cost and Usage Report**|Consultar informes detallados de costes y uso|

> [!TIP]  
> Para empezar, recuerda especialmente:
> 
> - **EC2:** Servidores.
>     
> - **S3:** Almacenamiento.
>     
> - **RDS:** Bases de datos.
>     
> - **VPC:** Redes.
>     
> - **IAM:** Permisos.
>     
> - **CloudWatch:** Monitorización.
>     

---

# 7. Marco de Adopción de la Nube (AWS CAF)

El **AWS Cloud Adoption Framework (CAF)** es un marco que ayuda a las empresas a organizar su transición a la nube.

Se divide en **6 perspectivas**.

## 7.1. Perspectiva de negocio

Busca que la tecnología ayude a conseguir los objetivos empresariales.

Incluye:

- Finanzas de TI.
    
- Estrategia tecnológica.
    
- Beneficios empresariales.
    
- Gestión de riesgos.
    

**Ejemplo:** Comprobar si migrar los servidores a AWS resulta rentable.

## 7.2. Perspectiva de personal

Prepara a los trabajadores para utilizar las nuevas tecnologías.

Incluye:

- Formación técnica.
    
- Gestión de empleados.
    
- Desarrollo profesional.
    
- Incentivos.
    
- Adaptación a cambios organizativos.
    

**Ejemplo:** Formar a los técnicos de una empresa para trabajar con AWS.

## 7.3. Perspectiva de gobernanza

Controla que las decisiones tecnológicas estén alineadas con los objetivos empresariales.

Incluye:

- Gestión de proyectos.
    
- Gestión de portafolios.
    
- Medición del rendimiento.
    
- Gestión de licencias.
    

**Ejemplo:** Supervisar que una migración a AWS cumpla el presupuesto y los objetivos.

## 7.4. Perspectiva de plataforma

Se encarga de diseñar y preparar la infraestructura tecnológica.

Incluye:

- Servidores.
    
- Redes.
    
- Almacenamiento.
    
- Bases de datos.
    
- Arquitectura de sistemas.
    
- Desarrollo de aplicaciones.
    

**Ejemplo:** Crear una infraestructura con EC2, VPC y RDS.

## 7.5. Perspectiva de seguridad

Garantiza que los sistemas y datos estén protegidos.

Incluye:

- Gestión de identidades y accesos.
    
- Detección de amenazas.
    
- Seguridad de infraestructura.
    
- Protección de datos.
    
- Respuesta a incidentes.
    

**Ejemplo:** Configurar IAM para que cada empleado tenga únicamente los permisos necesarios.

## 7.6. Perspectiva de operaciones

Se encarga de mantener los servicios funcionando correctamente.

Incluye:

- Monitorización de servicios.
    
- Monitorización del rendimiento.
    
- Inventario de recursos.
    
- Gestión de cambios y versiones.
    
- Informes y análisis.
    
- Recuperación ante desastres.
    
- Catálogo de servicios de TI.
    

**Ejemplo:** Utilizar CloudWatch para detectar problemas en un servidor.

---

## 8. Resumen de las seis perspectivas del AWS CAF

|Perspectiva|Objetivo principal|
|---|---|
|**Negocio**|Obtener beneficios empresariales|
|**Personal**|Preparar y formar trabajadores|
|**Gobernanza**|Controlar estrategias y procesos|
|**Plataforma**|Diseñar la infraestructura|
|**Seguridad**|Proteger sistemas y datos|
|**Operaciones**|Mantener los servicios funcionando|

> [!IMPORTANT]  
> **Para el examen:** Debes saber identificar las seis perspectivas del AWS CAF y reconocer su función principal.

---

## 9. Planificación de la adopción de la nube

La adopción de la nube requiere **planificación y coordinación** entre los departamentos de una empresa.

El **AWS CAF** ayuda a las organizaciones a:

- Planificar la migración a la nube.
    
- Identificar los cambios necesarios.
    
- Organizar las responsabilidades.
    
- Reducir riesgos.
    

Sus seis perspectivas permiten analizar las necesidades empresariales y tecnológicas.

---

## 10. Ahorro de costes mediante recursos bajo demanda

AWS permite utilizar recursos únicamente cuando se necesitan.

**Ejemplo:**

Una empresa necesita más servidores durante determinadas horas.

- **Infraestructura tradicional:** Debe comprar servidores capaces de soportar los momentos de máxima demanda.
    
- **AWS:** Puede iniciar instancias EC2 cuando las necesite y detenerlas cuando dejen de ser necesarias.
    

Esto permite reducir costes, dependiendo del tipo de instancia y de su configuración de facturación.

> [!IMPORTANT]  
> **Para el examen:** AWS puede resultar más económico porque permite ajustar los recursos a la demanda.

# 📝 Repaso rápido del módulo 1

**¿Qué es Cloud Computing?**  
Utilizar recursos informáticos a través de Internet bajo demanda.

**¿Qué diferencia existe entre IaaS, PaaS y SaaS?**  
Infraestructura, plataforma y software como servicio.

**¿Qué es CAPEX?**  
Gastos de capital, como comprar servidores.

**¿Qué es OPEX?**  
Gastos operativos, como pagar por recursos de AWS.

**¿Qué es AWS?**  
Una plataforma de servicios de computación en la nube.

**¿Qué es EC2?**  
Un servicio de servidores virtuales.

**¿Qué es S3?**  
Un servicio de almacenamiento de objetos.

**¿Qué es IAM?**  
Un servicio para gestionar identidades y permisos.

**¿Qué es AWS CAF?**  
Un marco que ayuda a las organizaciones a adoptar la nube.

**¿Cuántas perspectivas tiene AWS CAF?**  
Seis: negocio, personal, gobernanza, plataforma, seguridad y operaciones.