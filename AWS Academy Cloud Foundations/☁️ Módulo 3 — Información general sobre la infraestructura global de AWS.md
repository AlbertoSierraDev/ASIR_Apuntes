# 1. Infraestructura global de AWS

AWS dispone de una infraestructura distribuida por todo el mundo que permite ofrecer servicios en la nube.

Sus principales componentes son:

- **Regiones (Regions):** zonas geográficas donde AWS dispone de infraestructura.
    
- **Zonas de disponibilidad (Availability Zones):** ubicaciones aisladas dentro de una región.
    
- **Ubicaciones perimetrales (Edge Locations):** puntos que permiten entregar contenido cerca de los usuarios.
    

> [!IMPORTANT]  
> AWS utiliza esta infraestructura para mejorar la disponibilidad, la tolerancia a fallos y el rendimiento de sus servicios.

---

# 2. Regiones de AWS (Regions)

Una **región** es una ubicación geográfica donde AWS tiene centros de datos.

### Características

- Cada región contiene varias zonas de disponibilidad.
    
- Las regiones están separadas geográficamente.
    
- Permiten elegir dónde alojar los recursos y datos.
    
- No todos los servicios están disponibles en todas las regiones.
    

**Ejemplo:** Europa (España), identificada como `eu-south-2`.

### ¿Cómo elegir una región?

Se deben considerar:

1. **Latencia:** proximidad a los usuarios.
    
2. **Coste:** los precios pueden variar según la región.
    
3. **Servicios disponibles:** comprobar que la región ofrece los servicios necesarios.
    
4. **Cumplimiento legal:** requisitos sobre la ubicación de los datos.
    

---

# 3. Zonas de disponibilidad (Availability Zones)

Una **zona de disponibilidad (AZ)** es una ubicación aislada dentro de una región de AWS.

### Características

- Cada región dispone de varias zonas de disponibilidad.
    
- Cada zona contiene uno o más centros de datos.
    
- Están conectadas mediante redes de alta velocidad.
    
- Permiten mantener aplicaciones disponibles cuando falla otra zona.
    

**Ejemplo:**

Región: `eu-south-2`

Zonas de disponibilidad:

- `eu-south-2a`
    
- `eu-south-2b`
    
- `eu-south-2c`
    

### ¿Para qué sirven?

Para mejorar la **alta disponibilidad y la tolerancia a fallos**.

Si una aplicación utiliza varias zonas de disponibilidad, puede continuar funcionando aunque una de ellas falle, siempre que esté correctamente diseñada.

> [!IMPORTANT]  
> **Región:** ubicación geográfica.
> 
> **Zona de disponibilidad:** ubicación aislada dentro de una región.

---

# 4. Ubicaciones perimetrales (Edge Locations)

Las **Edge Locations** son ubicaciones de AWS distribuidas por el mundo que permiten entregar contenido cerca de los usuarios.

### Características

- Reducen la latencia.
    
- Mejoran la velocidad de entrega de contenido.
    
- Se utilizan con servicios como Amazon CloudFront.
    

### Amazon CloudFront

Es un servicio de distribución de contenido (**CDN**) que permite entregar páginas web, imágenes y vídeos rápidamente.

**Ejemplo:**

Un usuario de Madrid accede a una página web alojada en Estados Unidos.

CloudFront puede entregar contenido almacenado en caché desde una ubicación perimetral cercana a Madrid.

Esto reduce el tiempo de carga.

> [!IMPORTANT]  
> **CloudFront + Edge Locations = Menor latencia.**
> 
> Esta relación aparece en la pregunta oficial de ejemplo del módulo.

---

# 5. Servicios globales y regionales

Los servicios de AWS pueden tener un alcance global o regional.

### Servicios globales

No están limitados a una única región para su administración principal.

Ejemplos:

- **AWS IAM:** administración de identidades y permisos.
    
- **Amazon Route 53:** servicio de DNS.
    

### Servicios regionales

Sus recursos se administran dentro de regiones específicas.

Ejemplos:

- **Amazon EC2:** servidores virtuales.
    
- **AWS Lambda:** ejecución de código sin administrar servidores.
    
- **Amazon VPC:** redes virtuales privadas.
    

|Servicio|Alcance|
|---|---|
|AWS IAM|Global|
|Amazon Route 53|Global|
|Amazon EC2|Regional|
|AWS Lambda|Regional|
|Amazon VPC|Regional|

> [!IMPORTANT]  
> Para el examen:
> 
> - IAM y Route 53 → Globales.
>     
> - EC2 y Lambda → Regionales.
>     

---

# 6. Amazon VPC y subredes

## Amazon VPC

Amazon Virtual Private Cloud (VPC) permite crear una red virtual aislada dentro de AWS.

### Características

- Es un recurso regional.
    
- Permite organizar los recursos de red.
    
- Puede contener subredes en diferentes zonas de disponibilidad.
    

## Subredes (Subnets)

Una subred es una división de la red VPC.

### Características

- Pertenece a una única zona de disponibilidad.
    
- Permite organizar los recursos dentro de una VPC.
    

**Ejemplo:**

Región: `eu-south-2`

VPC: `10.0.0.0/16`

Subredes:

- Subred 1 → `eu-south-2a`
    
- Subred 2 → `eu-south-2b`
    
- Subred 3 → `eu-south-2c`
    

> [!IMPORTANT]  
> **VPC = Regional.**
> 
> **Subred = Zona de disponibilidad.**

---

# 7. Categorías de servicios de AWS

AWS organiza sus servicios en diferentes categorías según su función.

|Categoría|Servicio|Función|
|---|---|---|
|Cómputo|Amazon EC2|Servidores virtuales.|
|Cómputo|AWS Lambda|Ejecutar código sin administrar servidores.|
|Redes y entrega de contenido|Amazon VPC|Crear redes virtuales.|
|Redes y entrega de contenido|Amazon Route 53|Administrar DNS.|
|Redes y entrega de contenido|Amazon CloudFront|Distribuir contenido.|
|Seguridad, identidad y cumplimiento|AWS IAM|Gestionar usuarios y permisos.|
|Almacenamiento|Amazon S3|Almacenar objetos y archivos.|
|Bases de datos|Amazon RDS|Administrar bases de datos relacionales.|

### Conceptos importantes

- **IAM:** Seguridad, identidad y cumplimiento.
    
- **VPC:** Redes y entrega de contenido.
    
- **EC2:** Cómputo.
    

---

# 8. Consola de administración de AWS

La **Consola de administración de AWS** permite gestionar los servicios mediante una interfaz web.

### Funciones principales

- Buscar y acceder a servicios.
    
- Crear y administrar recursos.
    
- Cambiar entre regiones.
    
- Consultar configuraciones de los servicios.
    

### Selección de región

Desde la consola podemos seleccionar una región para administrar los recursos regionales.

**Ejemplo:**

Si creamos una instancia EC2 en Madrid, no aparecerá en la lista de instancias de otra región.

Esto ocurre porque EC2 es un servicio regional.

---

# 9. Preguntas importantes para el examen

### Pregunta 1

**¿A qué categoría pertenece AWS IAM?**

**Respuesta:** Seguridad, identidad y cumplimiento.

### Pregunta 2

**¿A qué categoría pertenece Amazon VPC?**

**Respuesta:** Redes y entrega de contenido.

### Pregunta 3

**¿Las subredes existen a nivel regional o de zona de disponibilidad?**

**Respuesta:** Zona de disponibilidad.

### Pregunta 4

**¿Las VPC existen a nivel regional o de zona de disponibilidad?**

**Respuesta:** Regional.

### Pregunta 5

**¿Qué servicios son globales entre EC2, IAM, Lambda y Route 53?**

**Respuesta:** IAM y Route 53.

### Pregunta 6 — Ejemplo oficial de AWS Academy

**¿Qué componente de la infraestructura global de AWS utiliza Amazon CloudFront para garantizar una entrega con baja latencia?**

A) Regiones de AWS.

B) Ubicaciones perimetrales de AWS.

C) Zonas de disponibilidad de AWS.

D) Amazon VPC.

**Respuesta correcta: B) Ubicaciones perimetrales de AWS.**

**Explicación:** CloudFront utiliza ubicaciones perimetrales para entregar contenido desde puntos cercanos a los usuarios.

---

# 10. Resumen del módulo

|Concepto|Qué debes recordar|
|---|---|
|Región|Ubicación geográfica de AWS.|
|Zona de disponibilidad|Ubicación aislada dentro de una región.|
|Edge Location|Entrega contenido cerca del usuario.|
|CloudFront|CDN que utiliza ubicaciones perimetrales.|
|IAM|Servicio global de identidades y permisos.|
|Route 53|Servicio global de DNS.|
|EC2|Servicio regional de servidores virtuales.|
|Lambda|Servicio regional de ejecución de código.|
|VPC|Red virtual de alcance regional.|
|Subred|Pertenece a una zona de disponibilidad.|

## 🎯 Lo más importante para el examen

1. **Regiones:** ubicaciones geográficas.
    
2. **Zonas de disponibilidad:** alta disponibilidad y tolerancia a fallos.
    
3. **Edge Locations:** baja latencia.
    
4. **CloudFront:** distribución rápida de contenido.
    
5. **IAM y Route 53:** servicios globales.
    
6. **EC2 y Lambda:** servicios regionales.
    
7. **VPC:** regional.
    
8. **Subred:** zona de disponibilidad.
    

---

# Fin del módulo 3

**AWS Academy Cloud Foundations — Información general sobre la infraestructura global de AWS.**

#AWS #AWSAcademy #CloudComputing #Infraestructura #CloudFoundations