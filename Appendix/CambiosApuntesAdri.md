# Cambios a partir de los apuntes de Adri (16/11)

Comparación de nuestros `.tex` con los apuntes de clase de Adri (Parte 1, Parte 2, Parte 3 Peano, Problemas 1 y Problemas 2).
Criterio: **añadir** siempre que se pueda; si algo nuestro no coincide con clase, se deja como **caso adicional** en vez de borrarlo.

Leyenda: `[+]` se añade · `[~]` se corrige o sustituye (se indica qué)

---

## Theory/1 - Sistemas lineales generales Teoría general.tex

### Funciones Lipschitzianas
- [+] Fecha histórica: funciones Lipschitzianas (Lipschitz, 1876).
- [+] Ejemplo $u^q$, $0<q<1$: es **globalmente** Lipschitz en $[\eta,+\infty)$ para cada $\eta>0$ ($\sup F' = q\,\eta^{q-1}$).
- [+] Criterio no autónomo ($\Rightarrow$): justificar $D_uf(t,u)\,v=\lim_{h\to0}\frac{f(t,u+hv)-f(t,u)}{h}$ mediante $f(t,u+w)=f(t,u)+D_uf\,w+o(\|w\|)$.
- [+] Ejemplo $\frac1t\sin u$: localmente Lipschitz uniformemente en $[\alpha,\beta]\subset(0,\infty)$ (corolario) y globalmente Lipschitz uniformemente en $J_\eta=[\eta,\infty)$.

### Teorema global de Cauchy-Lipschitz
- [+] Implicación $(\Leftarrow)$ de la formulación integral.
- [+] Equivalencia de la norma de Bielecki: $e^{-\gamma(\beta-\alpha)}\|u\|_\infty\le\|u\|_B\le\|u\|_\infty$.
- [+] Observación: el corolario vale para cualquier intervalo ($[\alpha,\beta)=\bigcup[\alpha,\beta-\frac1n]$, etc.).
- [+] Ejemplo de la versión relajada: $f=a(t)\sin u$ con $a\in\mathcal C(\mathbb R)$.

### Teorema local de Cauchy-Lipschitz
- [+] Apartado a) por continuidad: $U(t_0)=u_0$, luego $U$ no sale de la bola en algún $[t_0,t_0+\delta]$.
- [+] Frase clave de la unicidad: dos soluciones de $(P)$ serían dos soluciones de $(P_F)$.

### Solución maximal y teoremas fundamentales
- [+] Nombre "argumento de Wintner" para la existencia de $\lim_{t\to T_{\max}}u(t)=u^*$.
- [+] Nomenclatura: los $u_\omega$ del 3er TF son **ω-límites** de $\Gamma$.

### Ejemplos de aplicación
- [~] Logística: "competencia **inter**específica" → "**intra**específica".
- [+] Logística: casos $u_0\in[0,\lambda/a]$ (global), $u_0>\lambda/a$ (explota hacia el pasado), $u_0<0$ (explota hacia el futuro), con dibujo.
- [+] Volterra-Lotka generalizado (1926).
- [+] Kolmogorov con $v_0=0$: el caso de clase $\lambda=0$, $a=-1$ ($u'=u^2$, explota en $T_{\max}=1/u_0$, "puesto en un control"). **El nuestro ($a=+1$) se mantiene como caso adicional.**
- [+] Ejemplo $u'=|v|^p,\ v'=|u|^q$ ($p\ge q>1$): análisis completo de la explosión (identidad de energía, comparación $v'\ge Cv^\rho$, cota y fórmula de $T_{\max}$), incluido el caso $p=q$ ($T_{\max}=\frac{1}{p-1}$), que Adri dejó pendiente.

### Dependencia Lipschitziana
- [+] Motivación: logística $u(t;x,\lambda,a)$ y objetivo (regularidad de $u_0\mapsto u$, $f\mapsto u$).
- [~] Grönwall-Bellman: hipótesis como en clase ($x,y\in\mathcal C(J;\mathbb R)$, solo $p\ge0$). Se quita "no negativas" para $x,y$.
- [+] Grönwall: método de clase ("variación de coeficientes") como observación.
- [~] Dependencia Lipschitziana abstracta: "la fórmula del lema se simplifica a" → cálculo explícito por partes.
- [+] Teorema de dependencia respecto de datos iniciales: observación (condición suficiente: $\partial f_i/\partial u_j$ continuas) y citar el 1er TF en la prueba.
- [+] Ejemplo logístico de dependencia: $T_{\max}(x)\uparrow+\infty$ si $x\uparrow0$ y $T_{\min}(x)\to-\infty$ si $x\downarrow\lambda/a$.

## Theory/2 - Ecuaciones no lineales de segundo orden.tex
- Sin cambios (todo está). Nota de clase: "hay que saber pintar el potencial, entra en el examen" → se añade como observación.

## Theory/3 - Teoría de Peano.tex
- [+] Fechas: Ascoli-Arzelà (1883–1895, "nuestro nuevo teorema de la aplicación contractiva para esta parte"); Teorema global de Peano (1890).
- [+] Teorema de existencia de solución maximal, **enunciado mejorado**: toda solución local se prolonga a una maximal (no necesariamente única), con dibujo.
  - ⚠️ La demostración (con Zorn sobre las prolongaciones de la solución local) no está en los apuntes de Adri: la he redactado yo. Revisar.
  - Se añade en la propia demostración la nota "no se vio en clase" y la solución local de partida se llama $(\tilde I,\tilde u)$.
  - ⚠️ El dibujo de las soluciones maximales es orientativo (curvas aproximadas, no las soluciones exactas).
- [+] Nota: "hasta aquí el control" (Müller + introducción a sub/supersoluciones).

## Exercises/Hoja1.tex
- [~] Ej. 3: "Por el teorema de existencia y unicidad" → cadena de los tres teoremas + justificación de Lipschitz en $\Omega=(-1,\infty)$.
- [+] Ej. 3: caso $n=1$ ($a=0,b=1$) resuelto por separación de variables: llega a $-1$ en tiempo finito $T=-(1+u_0)-\ln|u_0|$. Caso $n=2$: $I=[0,+\infty)$.
- [+] Ej. 8: caso extra $\mu<0$ (de clase).
- [+] Ej. 10: integración explícita del sistema polar y aviso sobre $\theta=\arctan(v/u)$.
- [+] Ej. 11: "otra manera" con $T_{\max}=\int_1^\infty\frac{dx}{f(x)}=+\infty$.
- [~] Ej. 15: `medio` → `resuelto`. (La resolución ya estaba actualizada con el método de clase: variación de coeficientes + integral por partes "a la manera del profesor"; solo se cambia el estado.)

## Exercises/Hoja2.tex
- Ej. 3 y Ej. 4: ya transcritos desde Problemas 2 (no se tocan).
- [+] Ej. 3: comentario de clase "pensar qué pasa cuando $p\to1$ y $p\to\infty$".

---

**Estado:** todos los cambios aplicados y compilados sin errores (16/11).
