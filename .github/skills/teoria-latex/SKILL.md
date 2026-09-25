---
name: teoria-latex
description: Instrucciones y comandos precisos para formatear apuntes de teoría y ejercicios en LaTeX, basados en la estructura estándar de Métodos Numéricos y la Plantilla de Apuntes.
---
# Estilo de Apuntes LaTeX (Estándar UCM)

Esta skill define el formato exacto para tomar apuntes de teoría y ejercicios, basado en la estructura consolidada de la asignatura de Métodos Numéricos. Debes usar **exclusivamente** estos comandos y entornos personalizados que ya están definidos en el preámbulo.

## 1. Comandos de Teoría

Usa estos entornos para estructurar el contenido teórico. Siempre que sea posible, añade un título descriptivo entre corchetes.

*   **Definiciones:**
    `latex
    \begin{definición}[Título de la definición]
        Contenido de la definición...
    \end{definición}
    `
*   **Teoremas:**
    `latex
    \begin{teorema}[Título del teorema]
        Enunciado del teorema...
    \end{teorema}
    `
*   **Proposiciones:**
    `latex
    \begin{proposición}[Título de la proposición]
        Enunciado de la proposición...
    \end{proposición}
    `
*   **Demostraciones:**
    Usa el comando \dem (no el entorno proof habitual) que envuelve automáticamente el texto.
    `latex
    \dem{
        Aquí va el desarrollo de la demostración...
    }
    `
*   **Ejemplos:**
    Usa el comando \ejemplo (crea una caja coloreada especial).
    `latex
    \ejemplo{
        Aquí va el ejemplo desarrollado...
    }
    `
*   **Observaciones / Notas:**
    `latex
    \begin{observación}
        Nota aclaratoria o comentario importante...
    \end{observación}
    `

## 2. Comandos de Ejercicios

Para las hojas de problemas y exámenes, la plantilla cuenta con un sistema de cajas de colores que indican el estado del ejercicio.

*   **Inicio de una Hoja de Ejercicios:**
    Utiliza este comando para poner el título de la hoja y reiniciar automáticamente el contador de ejercicios.
    `latex
    \hojaejercicio{Título de la Hoja}
    `
*   **Estructura de un Ejercicio:**
    Usa el comando \ejercicio{estado}{marca}{Enunciado}{Solución}.
    `latex
    \ejercicio{estado}{marca}{
        Aquí va el enunciado del problema...
    }{
        Aquí va el desarrollo y la solución...
    }
    `
    *Parámetros importantes:*
    *   estado: Define el color de la caja. Puede ser:
        *   enunciado (Rojo): Ejercicio sin empezar.
        *   medio (Naranja): Ejercicio a medias o dudoso.
        *   esuelto (Verde): Ejercicio completado.
    *   marca: Úsalo para destacar ejercicios importantes o de examen (por ejemplo, pon x o déjalo vacío {}).

## 3. Normas Generales

1.  **No inventes entornos nuevos.** Limítate a usar los bloques de arriba para mantener la coherencia visual en todos los PDF de todas las asignaturas.
2.  **No uses \vspace ni formateos manuales** para separar teoremas o definiciones; los entornos mdframed del preámbulo ya calculan los márgenes.
3.  Usa los comandos matemáticos estándar definidos en el preámbulo (ej. \R, \C, \Q, \N, \Z).