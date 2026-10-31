---
tags:
  - programacion
  - dotnet
  - csharp
  - asir
aliases:
  - Apuntes de .NET y C#
---
# Apuntes de .NET y C#

> [!summary] Conceptos principales
> **.NET** es una plataforma de desarrollo, **C#** es un lenguaje de programación y el **SDK de .NET** contiene las herramientas para crear, compilar y ejecutar proyectos.

## 1. ¿Qué es .NET?

.NET permite desarrollar aplicaciones de consola, páginas web, API, servicios y otros tipos de aplicaciones. **ASP.NET Core** es el framework de .NET utilizado para desarrollar aplicaciones web y API.

- **C#:** lenguaje de programación con tipado estático.
- **SDK:** herramientas para desarrollar proyectos.
- **Runtime:** entorno necesario para ejecutar aplicaciones .NET.
- **NuGet:** gestor de paquetes y dependencias del ecosistema .NET.

## 2. Instalación y comprobación

Instala el SDK desde la [web oficial de .NET](https://dotnet.microsoft.com/download). Puedes utilizar Visual Studio o Visual Studio Code con soporte para C#.

```powershell
dotnet --version
dotnet --info
```

El primer comando muestra la versión del SDK seleccionada y el segundo, información del entorno.

## 3. Crear y ejecutar un proyecto

```powershell
mkdir MiPrimerProyecto
cd MiPrimerProyecto
dotnet new console
dotnet run
```

- `dotnet new console`: crea una aplicación de consola.
- `dotnet run`: compila y ejecuta el proyecto.
- `Program.cs`: archivo que contiene el punto de entrada en una aplicación de consola sencilla.
- `.csproj`: archivo de configuración del proyecto.

```csharp
Console.WriteLine("Hola, mundo");
Console.Write("Sin salto de línea");
```

En C#, las instrucciones suelen terminar en `;`. `WriteLine` añade un salto de línea; `Write` no.

## 4. Variables y tipos de datos

Una variable almacena un valor. C# utiliza **tipado estático**: el tipo de la variable se conoce y se comprueba.

| Tipo | Uso | Ejemplo |
|---|---|---|
| `string` | Texto | `"Madrid"` |
| `int` | Número entero | `24` |
| `double` | Número decimal | `1.72` |
| `decimal` | Decimal de alta precisión, habitual para importes | `19.99m` |
| `bool` | Verdadero o falso | `true` |
| `char` | Un carácter | `'A'` |

```csharp
string nombre = "Ana";
int edad = 24;
double altura = 1.72;
bool estudiante = true;
var ciudad = "Madrid"; // Se infiere string

edad = 25; // Válido
// edad = "veinticinco"; // Error: tipo incompatible
```

`var` **no significa que el tipo pueda cambiar**: el compilador infiere el tipo al declarar la variable.

### Constantes

```csharp
const double Pi = 3.14159;
```

Una constante no se puede reasignar.

## 5. Mostrar y leer información

```csharp
Console.Write("Nombre: ");
string nombre = Console.ReadLine() ?? "";
Console.WriteLine($"Hola, {nombre}");
```

- `Console.ReadLine()`: lee texto de la consola; puede devolver `null`.
- `?? ""`: utiliza una cadena vacía si el resultado es `null`.
- `$"...{variable}..."`: interpolación de cadenas.

Para convertir texto a un entero de manera segura:

```csharp
if (int.TryParse(Console.ReadLine(), out int edad))
{
    Console.WriteLine($"Edad: {edad}");
}
else
{
    Console.WriteLine("Número no válido");
}
```

`TryParse` devuelve `true` si la conversión se realiza correctamente.

## 6. Operadores

| Categoría | Operadores | Significado |
|---|---|---|
| Aritméticos | `+`, `-`, `*`, `/`, `%` | Suma, resta, multiplicación, división y resto |
| Comparación | `==`, `!=`, `>`, `<`, `>=`, `<=` | Comparan valores |
| Lógicos | `&&`, `\|\|`, `!` | Y, O, NO |
| Asignación | `=`, `+=`, `-=` | Asignar o actualizar |
| Incremento | `++`, `--` | Aumentar o disminuir en uno |

> [!note] División entre enteros
> `5 / 2` produce `2` si ambos operandos son enteros; `5.0 / 2` produce `2.5`.

## 7. Condicionales

### `if` / `else`

```csharp
int nota = 7;
if (nota >= 5)
{
    Console.WriteLine("Aprobado");
}
else
{
    Console.WriteLine("Suspenso");
}
```

### `switch`

```csharp
string dia = "lunes";
switch (dia)
{
    case "lunes":
        Console.WriteLine("Empieza la semana");
        break;
    default:
        Console.WriteLine("Otro día");
        break;
}
```

`if` permite comprobar condiciones; `switch` organiza diferentes casos de un valor.

## 8. Bucles

### `for`

Se utiliza habitualmente cuando se conoce el número de repeticiones.

```csharp
for (int i = 1; i <= 5; i++)
{
    Console.WriteLine(i);
}
```

### `while`

Repite el bloque mientras la condición sea verdadera.

```csharp
int contador = 0;
while (contador < 3)
{
    Console.WriteLine(contador);
    contador++;
}
```

### `foreach`

Recorre los elementos de una colección.

```csharp
string[] colores = { "rojo", "verde", "azul" };
foreach (string color in colores)
{
    Console.WriteLine(color);
}
```

`break` termina un bucle; `continue` pasa a la siguiente iteración.

## 9. Arrays y listas

### Array

Tiene longitud fija y los índices empiezan en `0`.

```csharp
string[] colores = { "rojo", "verde", "azul" };
Console.WriteLine(colores[0]); // rojo
Console.WriteLine(colores.Length); // 3
```

### `List<T>`

Colección cuyo tamaño puede cambiar.

```csharp
List<string> tareas = new List<string>();
tareas.Add("Estudiar C#");
tareas.Add("Repasar .NET");
tareas.Remove("Repasar .NET");
Console.WriteLine(tareas.Count);
```

- `Add()`: añade un elemento.
- `Remove()`: elimina una coincidencia.
- `Count`: número de elementos de una lista.
- `Length`: número de elementos de un array.

## 10. Métodos

Los métodos agrupan instrucciones reutilizables. Pueden recibir **parámetros** y devolver un resultado mediante `return`.

```csharp
static int Sumar(int a, int b)
{
    return a + b;
}

int resultado = Sumar(4, 6);
Console.WriteLine(resultado); // 10
```

- `static`: el método pertenece al tipo, no a una instancia.
- `int`: tipo del valor devuelto.
- `void`: indica que el método no devuelve un valor.

## 11. Clases y objetos

Una **clase** define propiedades y comportamientos; un **objeto** es una instancia de esa clase.

Archivo `Persona.cs`:

```csharp
public class Persona
{
    public string Nombre { get; set; } = "";
    public int Edad { get; set; }

    public void Saludar()
    {
        Console.WriteLine($"Hola, soy {Nombre}");
    }
}
```

En `Program.cs`:

```csharp
Persona persona = new Persona();
persona.Nombre = "Ana";
persona.Edad = 24;
persona.Saludar();
```

- `class`: declara una clase.
- `new`: crea una instancia.
- `{ get; set; }`: permite leer y modificar una propiedad.
- `public`: permite acceder al miembro desde código donde sea visible.

## 12. Errores y excepciones

- **Error de compilación:** impide compilar el programa.
- **Excepción:** error o situación anómala que aparece durante la ejecución.

```csharp
try
{
    int numero = int.Parse("abc");
    Console.WriteLine(numero);
}
catch (FormatException)
{
    Console.WriteLine("Formato numérico incorrecto");
}
```

Para datos introducidos por el usuario, normalmente se prefiere `TryParse` a utilizar excepciones como mecanismo habitual de validación.

## 13. Comandos esenciales de .NET

| Comando | Función |
|---|---|
| `dotnet --version` | Muestra la versión del SDK |
| `dotnet --info` | Muestra información de .NET |
| `dotnet new console` | Crea un proyecto de consola |
| `dotnet new list` | Muestra las plantillas disponibles |
| `dotnet run` | Compila y ejecuta |
| `dotnet build` | Compila el proyecto |
| `dotnet test` | Ejecuta pruebas configuradas |
| `dotnet clean` | Limpia resultados de compilación |
| `dotnet add package NOMBRE` | Añade un paquete NuGet (sintaxis habitual en SDK anteriores; en SDK recientes también existe `dotnet package add`) |
| `dotnet --help` | Muestra ayuda |

## 14. Introducción a ASP.NET Core

ASP.NET Core permite crear aplicaciones web y **API HTTP**. Una API expone rutas a las que pueden acceder otras aplicaciones.

Crear un proyecto web mínimo:

```powershell
dotnet new web -n MiApi
cd MiApi
dotnet run
```

Ejemplo de `Program.cs`:

```csharp
var builder = WebApplication.CreateBuilder(args);
var app = builder.Build();

app.MapGet("/", () => "Hola desde mi API");
app.MapGet("/saludo/{nombre}", (string nombre) => $"Hola, {nombre}");

app.Run();
```

- `WebApplication.CreateBuilder(args)`: prepara la configuración de la aplicación.
- `builder.Build()`: construye la aplicación.
- `MapGet(...)`: define una ruta que responde a solicitudes HTTP GET.
- `app.Run()`: inicia la aplicación web.

## 15. Errores frecuentes

| Mensaje o código | Causa habitual |
|---|---|
| `dotnet no se reconoce` | El SDK no está instalado o no está disponible en `PATH` |
| No se encuentra un proyecto | La terminal está fuera de la carpeta con el `.csproj` |
| `CS0029` | Conversión o asignación entre tipos incompatibles |
| `CS1002` | Falta un punto y coma `;` |
| `NullReferenceException` | Se intenta utilizar una referencia `null` |

## 16. Recursos oficiales

- [Documentación de .NET](https://learn.microsoft.com/dotnet/)
- [Documentación de C#](https://learn.microsoft.com/dotnet/csharp/)
- [Descargar .NET](https://dotnet.microsoft.com/download)

---

> [!tip] Resumen rápido
> **.NET = plataforma** · **C# = lenguaje** · **SDK = herramientas de desarrollo** · **ASP.NET Core = desarrollo web y API** · **NuGet = paquetes**.
