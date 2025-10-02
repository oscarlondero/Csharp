# ENUNCIADO DEL PROYECTO
## Sistema de Gestión de Figuras Geométricas

---

## INFORMACIÓN GENERAL

**Título del Proyecto:** Sistema de Gestión de Figuras Geométricas
**Lenguaje:** C#
**Paradigma:** Programación Orientada a Objetos (POO)
**Tipo de Proyecto:** Sistema de gestión de figuras geométricas con herencia y polimorfismo
**Nivel:** Intermedio
**Duración Estimada:** 7 días de desarrollo

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
[ ] Screenshots de la ejecución del programa mostrando los resultados.

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

Ejemplos de preguntas en defensa:

"¿Por qué la clase Figura es abstracta?"
"¿Cómo funciona el polimorfismo en este proyecto?"
"Modifique la clase Circulo para que tenga una propiedad Diametro."
"Agregue una nueva clase Cuadrado que herede de Figura."

Documentación Obligatoria del Uso de IA
Para promover transparencia académica, reflexión metacognitiva y aprendizaje profundo, todos los estudiantes deben entregar DOS archivos de documentación junto con el proyecto:

📄 Archivo 1: ai_declaration.md (Declaración de Uso de IA)
Este archivo documenta qué código fue generado por IA y cómo se modificó.

Estructura obligatoria:

# 🤖 Declaración de Uso de IA 🤖

1. He utilizado herramientas de IA en este entregable: [✅ Sí / ❌ No]

2. Herramienta(s) utilizada(s):
   - [Nombre de la herramienta y versión]

3. Partes del entregable generadas por IA (ficheros/clases/métodos/fragmentos de código):
   - [Lista específica de clases/métodos/secciones generadas]
   - Ejemplo: "Clase `Circulo` (versión inicial)"
   - Ejemplo: "Esquema inicial de clases `Figura`, `Circulo`, `Rectangulo`, `Triangulo`"

4. Modificaciones realizadas sobre la salida de la IA:
   - [Describir cambios específicos y el MOTIVO de cada cambio]
   - Ejemplo: "Se agregó la propiedad `Nombre` a la clase `Figura`. **Motivo:** Era un requisito del proyecto."
   - Ejemplo: "Se corrigió el cálculo del área del triángulo. **Motivo:** La IA usó una fórmula incorrecta."

5. Fecha y enlace a la captura de la conversación o archivo con la salida original de la IA:
   - Fecha: [YYYY-MM-DD]
   - Enlace/Archivo: [Incluir screenshot o archivo de texto con la conversación completa]

6. Consideraciones éticas (opcional):
   - [Reflexión sobre el uso de IA y la originalidad del trabajo]
Nivel de detalle esperado:

❌ Incorrecto: "La IA generó el código"
✅ Correcto: "ChatGPT generó las clases Figura, Circulo, Rectangulo y Triangulo (versión inicial). Se modificó la clase Figura para agregar la propiedad Nombre y se corrigió el cálculo del área del triángulo."
📄 Archivo 2: metacognition.md (Informe de Metacognición)
Este archivo documenta el proceso de aprendizaje y reflexión crítica sobre el trabajo realizado.

Estructura obligatoria:

# 🤔 Informe de Metacognición 🤔

## 1. 🎯 Objetivo del entregable
[Describir en 2-3 párrafos qué se debía lograr con este proyecto]

## 2. 👣 Pasos realizados (herramientas, recursos, tiempo invertido)
1. [Paso 1 con herramientas específicas y tiempo]
   - Ejemplo: "Investigación sobre herencia en C# (2 horas): Consulté la documentación de Microsoft sobre herencia."
2. [Paso 2]
3. [Etc.]

## 3. 🤯 Dificultades encontradas y cómo se resolvieron
- **Dificultad 1:** [Descripción detallada]
  - **¿Por qué fue difícil?:** [Explicación]
  - **¿Cómo se resolvió?:** [Solución específica]
  - **Estrategias utilizadas:** [Debugging, búsqueda en Stack Overflow, experimentación, etc.]

## 4. 🤖 Si usé IA: prompt(s) usados, salida recibida y cambios realizados

### Prompt 1:
- **Prompt:** "[Texto exacto del prompt]"
- **Salida (resumen):** "[Resumen de lo que generó la IA]"
- **Modificaciones:** "[Cambios específicos realizados]"
- **Efectividad del prompt:** "[¿Funcionó bien? ¿Qué se podría mejorar?]"

### Prompt 2:
[Repetir estructura]

## 5. 🎓 Qué aprendí de esta actividad
- [Lista de aprendizajes específicos, no generales]
- Ejemplo correcto: "Aprendí que la herencia en C# se implementa con el operador `:` y que los métodos abstractos se definen con la palabra clave `abstract`."
- Ejemplo incorrecto: "Aprendí sobre C#." (demasiado general)

### ¿Cómo afectó el uso de IA mi aprendizaje?
[Reflexión sobre si la IA aceleró/dificultó el aprendizaje, si generó nuevas preguntas, etc.]

## 6. 🤔 Consideraciones éticas (opcional)
[Reflexión sobre la autoría del código, transparencia, y uso responsable de IA]
Nivel de detalle esperado:

❌ Incorrecto: "Tuve problemas con la herencia."
✅ Correcto: "La herencia fue difícil porque no entendía cómo implementar métodos abstractos. Investigué en la documentación de Microsoft y aprendí que los métodos abstractos se definen con la palabra clave abstract y que las clases derivadas deben implementar estos métodos."
Propósito de los Archivos de Documentación
Estos archivos buscan:

Transparencia total: Saber exactamente qué código es original vs. generado por IA
Aprendizaje profundo: Reflexionar sobre el proceso, no solo el resultado
Pensamiento crítico: Analizar la efectividad de los prompts y las limitaciones de la IA
Evaluación justa: Permitir al evaluador entender el nivel de comprensión real
Honestidad académica: Promover la integridad sin penalizar el uso de herramientas modernas
Importante: El uso de IA NO reduce la calificación si está bien documentado. Lo que se evalúa es:

✅ La capacidad de modificar el código generado
✅ La comprensión profunda del código final
✅ La reflexión crítica sobre el proceso
✅ La habilidad de explicar decisiones
Penalizaciones:

❌ No entregar ai_declaration.md o metacognition.md → -10 puntos
❌ Documentación superficial o genérica → -5 puntos
❌ No poder explicar el código en la defensa → Hasta -30 puntos
CRONOGRAMA SUGERIDO
Semana	Actividad	Horas
1	Estructura base + Herencia + Abstracción	8-10
2	Implementación de Clases Derivadas + Polimorfismo	10-12
3	Implementación de GestorFiguras + Pruebas	8-10
4	Documentación + Refinamiento	6-8
Total estimado: 32-40 horas

CONTACTO Y SOPORTE
Para consultas sobre el proyecto:

Revisar la documentación de C#
Consultar la documentación de Microsoft sobre POO
