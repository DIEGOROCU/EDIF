---
name: teoria-latex
description: Instrucciones y comandos precisos para formatear apuntes de teoría y ejercicios en LaTeX, basados en el estilo personal del usuario y la Plantilla de Apuntes de la UCM.
---
# Estilo de Apuntes LaTeX (Estándar UCM)

Esta skill define el formato exacto, los comandos y el estilo de redacción para tomar apuntes de teoría y ejercicios. Se basa en el estándar y la voz del autor de la asignatura de Métodos Numéricos y Ecuaciones Algebraicas. 

## 1. Comandos de Teoría

Usa **exclusivamente** estos entornos predefinidos en el preámbulo. Siempre que sea posible, añade un título descriptivo entre corchetes.

*   **Definiciones:**
    `latex
    \begin{definición}[Título de la definición]
        Contenido de la definición...
    \end{definición}
    `
*   **Teoremas y Proposiciones:**
    `latex
    \begin{teorema}[Título del teorema]
        Enunciado del teorema...
    \end{teorema}
    
    \begin{proposición}[Título de la proposición]
        Enunciado de la proposición...
    \end{proposición}
    `
*   **Demostraciones:**
    Usa el entorno estándar proof. **No** uses comandos envolventes como \dem{...}.
    `latex
    \begin{proof}
        Aquí va el desarrollo desglosado de la demostración...
    \end{proof}
    `
*   **Ejemplos:**
    Usa el comando especial \ejemplo{...} que genera una caja coloreada.
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

## 2. Jerarquía y Estructura (Sections)

El texto debe fluir de forma estructurada usando la jerarquía estándar:
*   \section{Título del Tema}: Corresponde al gran bloque o capítulo general (ej. "Extensiones de cuerpos").
*   \subsection{Concepto Principal}: Divide el tema en los pilares fundamentales o teóricos (ej. "Conceptos básicos", "Característica", "El grado de una extensión").
*   \subsubsection{Detalle o Teorema Clave}: Se usa para dar granularidad aislando un subconcepto o un cálculo importante. **También es obligatorio usarlo para enmarcar y darle peso a los teoremas muy importantes del curso**, asumiendo que dichos teoremas no abarquen lo suficiente como para merecer su propia \subsection directa.

## 3. Estilo de Redacción y Rigor Matemático

*   **Prosa conectiva:** No apiles definiciones y teoremas como si fuera un diccionario inconexo. Escribe siempre pequeñas frases introductorias o de transición (ej: *"Veamos algunos tipos de matrices que nos encontraremos..."*, *"Para entender su estructura, consideramos..."*).
*   **Desglose visual (itemize):** Cuando haya múltiples propiedades, ejemplos o tipos, no uses párrafos largos de texto corrido; utiliza \begin{itemize} y destaca el término clave con \textbf{}.
*   **Fórmulas y Ecuaciones:** 
    *   Usa **únicamente** el modo "display" \[ ... \] para destacar ecuaciones clave o desarrollos de fórmulas.
    *   **Estrictamente prohibido el uso de \begin{align} o \begin{align*}**. Si hay múltiples líneas, resuélvelo dentro de \[ ... \] usando saltos o separándolo en varias ecuaciones.
    *   Usa el modo "inline" $ ... $ para variables sueltas y operaciones cortas en el propio texto.
*   **Demostraciones sin magia:** Al rellenar una \begin{proof}, no asumas saltos lógicos. Explica explícitamente el porqué de cada paso analítico (ej: mencionar explícitamente si aplicas la hipótesis inductiva, un teorema de isomorfía, o justificar que el núcleo es cero).

## 4. Comandos de Ejercicios

Para las hojas de problemas y exámenes, utiliza el sistema de cajas de colores de la plantilla.

*   **Inicio de Hoja:**
    `latex
    \hojaejercicio{Título de la Hoja}
    `
*   **Estructura de un Ejercicio:**
    `latex
    \ejercicio{estado}{marca}{
        Enunciado del problema...
    }{
        Desarrollo y solución paso a paso...
    }
    `
    *Estados posibles:* enunciado (Rojo), medio (Naranja), esuelto (Verde).
    *Marca:* Úsalo para destacar (x) o déjalo vacío ({}).

## 5. Reglas de Intervención (Modo de actuar de la IA)

1.  **Edición Aditiva:** Cuando corrijas o mejores los apuntes, actúa añadiendo explicaciones, pero **no elimines el texto original** ni borres la voz del autor.
2.  **No inventes formatos:** No uses \vspace, \newline forzados ni inventes entornos. Los espacios los calcula el paquete mdframed.
3.  **Consistencia de notación:** Usa los macros matemáticos predefinidos (\R, \C, \Q, \N, \Z) y respeta estrictamente cómo el autor haya llamado a sus variables en el documento.