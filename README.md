# Csharp
Proyecto educativo C#
# Sistema de Gestión de Figuras Geométricas (C#)

![C# Version](https://img.shields.io/badge/c%23--blue)
![License](https://img.shields.io/badge/license-Educational-green)

Sistema de gestión de figuras geométricas implementado en **C#** utilizando **paradigma de Programación Orientada a Objetos (POO)**. Desarrollado como proyecto educativo para demostrar conceptos básicos de POO, herencia, abstracción y polimorfismo.

---

## 📋 Tabla de Contenidos

- [Características](#características)
- [Requisitos](#requisitos)
- [Uso](#uso)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Clases y Métodos](#clases-y-métodos)
- [Ejemplos de Uso](#ejemplos-de-uso)
- [Licencia](#licencia)

---

## 🎯 Características

### Gestión de Figuras Geométricas

- **📐 Clase Base `Figura`**
  - Propiedad `Nombre` (string)
  - Métodos abstractos: `CalcularArea()`, `CalcularPerimetro()`
  - Método virtual: `MostrarDatos()`

- **🔵 Clase Derivada `Circulo`**
  - Propiedad `Radio` (double)
  - Implementación de `CalcularArea()` y `CalcularPerimetro()`

- **📏 Clase Derivada `Rectangulo`**
  - Propiedades `Base` y `Altura` (double)
  - Implementación de `CalcularArea()` y `CalcularPerimetro()`

- **📐 Clase Derivada `Triangulo`**
  - Propiedades `LadoA`, `LadoB` y `LadoC` (double)
  - Implementación de `CalcularArea()` (fórmula de Herón) y `CalcularPerimetro()`

- **🧮 Clase `GestorFiguras`**
  - Lista de objetos `Figura`
  - Métodos para agregar, eliminar y mostrar figuras
  - Métodos para calcular el área y perímetro total de las figuras

---

## 💻 Requisitos

### Requisitos de Sistema

- **.NET SDK** (versión compatible con C#)
- Sistema operativo: Windows, Linux o macOS
- Entorno de desarrollo integrado (IDE) como Visual Studio o Visual Studio Code (con extensiones de C#)

---

## 🎮 Uso

### Compilar y Ejecutar el Proyecto

1.  Abre el proyecto en tu IDE preferido.
2.  Compila el proyecto.
3.  Ejecuta el programa.

### Interacción

El programa crea instancias de las clases `Circulo`, `Rectangulo` y `Triangulo`, las agrega a la clase `GestorFiguras` y muestra los datos de cada figura, así como el área y perímetro total.

---

## 📁 Estructura del Proyecto
FigurasGeometricas/ ├── Figura.cs # Clase base abstracta Figura ├── Circulo.cs # Clase derivada Circulo ├── Rectangulo.cs # Clase derivada Rectangulo ├── Triangulo.cs # Clase derivada Triangulo ├── GestorFiguras.cs # Clase GestorFiguras para gestionar la lista de figuras ├── Program.cs # Archivo principal con el método Main └── FigurasGeometricas.csproj # Archivo de proyecto de C#


---

## 🛠️ Clases y Métodos

### Clase `Figura`

-   **Propiedades:**
    -   `Nombre` (string): Nombre de la figura.
-   **Métodos:**
    -   `CalcularArea()` (abstract double): Método abstracto para calcular el área.
    -   `CalcularPerimetro()` (abstract double): Método abstracto para calcular el perímetro.
    -   `MostrarDatos()` (virtual void): Muestra el nombre, área y perímetro de la figura.

### Clase `Circulo`

-   **Propiedades:**
    -   `Radio` (double): Radio del círculo.
-   **Métodos:**
    -   `CalcularArea()` (override double): Calcula el área del círculo.
    -   `CalcularPerimetro()` (override double): Calcula el perímetro del círculo.

### Clase `Rectangulo`

-   **Propiedades:**
    -   `Base` (double): Base del rectángulo.
    -   `Altura` (double): Altura del rectángulo.
-   **Métodos:**
    -   `CalcularArea()` (override double): Calcula el área del rectángulo.
    -   `CalcularPerimetro()` (override double): Calcula el perímetro del rectángulo.

### Clase `Triangulo`

-   **Propiedades:**
    -   `LadoA` (double): Lado A del triángulo.
    -   `LadoB` (double): Lado B del triángulo.
    -   `LadoC` (double): Lado C del triángulo.
-   **Métodos:**
    -   `CalcularArea()` (override double): Calcula el área del triángulo (fórmula de Herón).
    -   `CalcularPerimetro()` (override double): Calcula el perímetro del triángulo.

### Clase `GestorFiguras`

-   **Propiedades:**
    -   `ListaFiguras` (List\<Figura>): Lista para almacenar las figuras.
-   **Métodos:**
    -   `AgregarFigura(Figura figura)`: Agrega una figura a la lista.
    -   `EliminarFigura(string nombre)`: Elimina una figura de la lista por nombre.
    -   `MostrarTodasLasFiguras()`: Muestra los datos de todas las figuras en la lista.
    -   `CalcularAreaTotal()`: Calcula el área total de todas las figuras.
    -   `CalcularPerimetroTotal()`: Calcula el perímetro total de todas las figuras.

---

## 💡 Ejemplos de Uso

### Creación y Gestión de Figuras

```csharp
GestorFiguras gestor = new GestorFiguras();

Circulo circulo1 = new Circulo("Círculo 1", 5);
Rectangulo rectangulo1 = new Rectangulo("Rectángulo A", 4, 6);
Triangulo triangulo1 = new Triangulo("Triángulo 1", 3, 4, 5);

gestor.AgregarFigura(circulo1);
gestor.AgregarFigura(rectangulo1);
gestor.AgregarFigura(triangulo1);

gestor.MostrarTodasLasFiguras();

Console.WriteLine($"Área Total: {gestor.CalcularAreaTotal()}");
Console.WriteLine($"Perímetro Total: {gestor.CalcularPerimetroTotal()}");
```
---


### 📄 Licencia
- Este proyecto es de uso educativo y está disponible para fines de aprendizaje.
- Desarrollado como proyecto educativo de Programación Orientada a Objetos en C#
