# ENUNCIADO DEL PROYECTO
## Sistema de Gestión de Figuras Geométricas

---

## INFORMACIÓN GENERAL

**Título del Proyecto:** Sistema de Gestión de Figuras Geométricas
**Lenguaje:** C#
**Paradigma:** Programación Orientada a Objetos (POO)
**Tipo de Proyecto:** Sistema de gestión de figuras geométricas con herencia y polimorfismo
**Nivel:** Intermedio
**Duración Estimada:** 3-4 semanas de desarrollo

---

## DESCRIPCIÓN DEL PROYECTO

Se requiere desarrollar un **sistema de gestión de figuras geométricas** implementado en C#, utilizando el paradigma de Programación Orientada a Objetos (POO). El sistema debe gestionar diferentes tipos de figuras geométricas (círculos, rectángulos, triángulos) utilizando conceptos de herencia, abstracción y polimorfismo.

Este proyecto educativo tiene como objetivo demostrar conceptos básicos de:
- Programación Orientada a Objetos en C#
- Herencia y clases abstractas
- Polimorfismo
- Encapsulamiento
- Uso de listas y objetos

---

## OBJETIVOS DE APRENDIZAJE

Al completar este proyecto, el estudiante será capaz de:

1. **Aplicar principios de programación orientada a objetos** utilizando clases, herencia y polimorfismo.
2. **Implementar clases abstractas** y métodos abstractos.
3. **Utilizar herencia** para crear clases derivadas que hereden de una clase base.
4. **Implementar polimorfismo** mediante métodos virtuales y overrides.
5. **Utilizar listas** para gestionar colecciones de objetos.
6. **Aplicar encapsulamiento** mediante propiedades con `get` y `set`.
7. **Diseñar un sistema** con múltiples clases interrelacionadas.

---

## REQUISITOS TÉCNICOS

### Requisitos Obligatorios

#### 1. Lenguaje y Entorno
- **C#**
- **.NET SDK** (versión compatible con C#)
- Entorno de desarrollo integrado (IDE) como Visual Studio o Visual Studio Code (con extensiones de C#)

#### 2. Paradigma de Programación
- **100% Programación Orientada a Objetos**
- Uso de clases, herencia y polimorfismo
- Uso de clases abstractas y métodos abstractos

#### 3. Estructura del Proyecto
- Clase base abstracta `Figura`
- Clases derivadas: `Circulo`, `Rectangulo`, `Triangulo`
- Clase `GestorFiguras` para gestionar la lista de figuras

#### 4. Restricciones Técnicas Específicas

**OBLIGATORIO:**
- ✅ Clase base abstracta `Figura` con métodos abstractos `CalcularArea()` y `CalcularPerimetro()`
- ✅ Clases derivadas `Circulo`, `Rectangulo`, `Triangulo` que implementen los métodos abstractos
- ✅ Clase `GestorFiguras` para gestionar la lista de figuras
- ✅ Uso de propiedades con `get` y `set` para encapsulamiento
- ✅ Uso de listas para almacenar objetos de tipo `Figura`
- ✅ Método virtual `MostrarDatos()` en la clase base `Figura` que pueda ser sobreescrito en las clases derivadas

---

## FUNCIONALIDADES REQUERIDAS

### 1. CLASE BASE `Figura`

- Propiedad `Nombre` (string)
- Métodos abstractos: `CalcularArea()`, `CalcularPerimetro()`
- Método virtual: `MostrarDatos()`

### 2. CLASE DERIVADA `Circulo`

- Propiedad `Radio` (double)
- Implementación de `CalcularArea()`: `Math.PI * Radio * Radio`
- Implementación de `CalcularPerimetro()`: `2 * Math.PI * Radio`

### 3. CLASE DERIVADA `Rectangulo`

- Propiedades `Base` y `Altura` (double)
- Implementación de `CalcularArea()`: `Base * Altura`
- Implementación de `CalcularPerimetro()`: `2 * (Base + Altura)`

### 4. CLASE DERIVADA `Triangulo`

- Propiedades `LadoA`, `LadoB` y `LadoC` (double)
- Implementación de `CalcularArea()`: (Utilizar la fórmula de Herón)
- Implementación de `CalcularPerimetro()`: `LadoA + LadoB + LadoC`

### 5. CLASE `GestorFiguras`

- Lista de objetos `Figura`
- Métodos para agregar, eliminar y mostrar figuras
- Métodos para calcular el área y perímetro total de las figuras

---

## ESTRUCTURA DE CLASES

### Clase `Figura`
```csharp
public abstract class Figura
{
    public string Nombre { get; set; }
    public abstract double CalcularArea();
    public abstract double CalcularPerimetro();
    public virtual void MostrarDatos();
}
Clase Circulo
public class Circulo : Figura
{
    public double Radio { get; set; }
    public override double CalcularArea();
    public override double CalcularPerimetro();
}
Clase Rectangulo
public class Rectangulo : Figura
{
    public double Base { get; set; }
    public double Altura { get; set; }
    public override double CalcularArea();
    public override double CalcularPerimetro();
}
Clase Triangulo
public class Triangulo : Figura
{
    public double LadoA { get; set; }
    public double LadoB { get; set; }
    public double LadoC { get; set; }
    public override double CalcularArea();
    public override double CalcularPerimetro();
}
Clase GestorFiguras
public class GestorFiguras
{
    public List<Figura> ListaFiguras { get; set; }
    public void AgregarFigura(Figura figura);
    public void EliminarFigura(string nombre);
    public void MostrarTodasLasFiguras();
    public double CalcularAreaTotal();
    public double CalcularPerimetroTotal();
}
CRITERIOS DE EVALUACIÓN
Distribución de Puntuación (100 puntos)
Categoría	Peso	Puntos	Descripción
Herencia y Abstracción	30%	30 pts	Correcta implementación de la clase base Figura y las clases derivadas.
Polimorfismo	20%	20 pts	Uso correcto de métodos virtuales y overrides.
Encapsulamiento	15%	15 pts	Uso de propiedades con get y set.
Gestión de Figuras	15%	15 pts	Implementación de la clase GestorFiguras y sus métodos.
Calidad del Código	10%	10 pts	Código limpio, legible y bien documentado.
Funcionalidad	10%	10 pts	El programa debe compilar y ejecutar correctamente, mostrando los resultados esperados.

ENTREGABLES
1. Código Fuente
[ ] Figura.cs
[ ] Circulo.cs
[ ] Rectangulo.cs
[ ] Triangulo.cs
[ ] GestorFiguras.cs
[ ] Program.cs
[ ] Código funcional y ejecutable
[ ] Cumple todas las restricciones técnicas

2. Documentación
[ ] README.md (documentación del proyecto)

3. Evidencia de Pruebas
[ ] Video con cámara encendida de 7-10 minutos compartiendo pantalla explicando el código y el funcionamiento del programa.

USO DE INTELIGENCIA ARTIFICIAL
¿Se Permite el Uso de IA?
SÍ, se permite y se fomenta el uso de herramientas de IA para el desarrollo de este proyecto, incluyendo pero no limitado a:

Max
ChatGPT
GitHub Copilot
Gemini
Cursor AI
Otras herramientas de asistencia de código

Condiciones de Uso
✅ PERMITIDO:
Generación de código con asistentes de IA
Debugging con ayuda de IA
Optimización de funciones existentes
Documentación (comentarios)
Explicaciones de conceptos y soluciones
Refactoring guiado por IA
Generación de datos de prueba
Consultas sobre mejores prácticas

⚠️ RESPONSABILIDADES DEL ESTUDIANTE:
Comprender el código generado

Debe poder explicar cada clase y método implementado
Debe entender la lógica de negocio
Debe ser capaz de modificar el código generado
Validar funcionalidad

Probar todas las clases y métodos exhaustivamente
Verificar que cumplan con los requisitos del proyecto
Adaptar a las especificaciones

La IA puede generar código que no cumpla las restricciones
El estudiante debe modificar el código para cumplir requisitos

Evaluación con Uso de IA
Durante la defensa del proyecto, el estudiante debe demostrar:

Conocimiento profundo del código implementado
Capacidad de modificación en vivo
Comprensión de decisiones arquitectónicas
Habilidad de debugging sin asistencia de IA

Tests y preguntas para desarrollar en video de la defensa del proyecto:

"¿Por qué la clase Figura es abstracta?"
"¿Cómo funciona el polimorfismo en este proyecto?"
"Modifique la clase Circulo para que tenga una propiedad Diametro."
"Agregue una nueva clase Cuadrado que herede de Figura."

Documentación Obligatoria del Uso de IA
Para promover transparencia académica, reflexión metacognitiva y aprendizaje profundo, todos los estudiantes deben entregar el archivo que documenta qué código fue generado por IA y cómo se modificó. Detallando herramienta de IA  utilizada y los textos de los prompts con sus respuestas.

CRONOGRAMA SUGERIDO

Semana	Actividad	                                        Horas
----------------------------------------------------------------------
1	    Estructura base + Herencia + Abstracción	        8-10
2	    Implementación de Clases Derivadas + Polimorfismo	10-12
3	    Implementación de GestorFiguras + Pruebas	        8-10
4	    Documentación + Refinamiento	                    6-8
----------------------------------------------------------------------
Total estimado:                                         32-40 horas (2 intervenciones semanales de 3-5 horas cada una)

CONTACTO Y SOPORTE
Para consultas sobre el proyecto: Profesores de cátedra.

