# Cambios:

- Revisar teorema local de Cauchy-Lipschitz y su demostración.
- Revisar teorema global de Cauchy-Lipschitz y su demostración.
- Revisar la demostración del teorema de unicidad global
- Revisar el inicio de la demostración del 4 teorema fundamental

---

## Revisión hecha (16/11), comparando con los apuntes de clase (Parte 1 de Adri y fotos de Jorge)

### Teorema global de Cauchy-Lipschitz ✅
- La estimación de la contracción solo estaba hecha para $t \ge t_0$ (con $e^{\gamma(s-t_0)}$), y el caso $t<t_0$ se despachaba con "razonamiento simétrico".
- Rehecha como en clase, con $e^{-\gamma|t-t_0|}$ e integrando entre $\min\{t_0,t\}$ y $\max\{t_0,t\}$; vale para todo $t$.
- Se calcula $\int e^{\gamma|s-t_0|}ds=\frac{e^{\gamma|t-t_0|}-1}{\gamma}$ y se obtiene $\frac{L}{\gamma}(1-e^{-\gamma|t-t_0|})\le\frac{L}{\gamma}$.
- Nota: en clase se toma $B=2L$, que da contracción $\frac12$.

### Teorema local de Cauchy-Lipschitz ✅
- Enunciado:
  - el apartado a) decía "única solución" y en clase es "una solución, **al menos**";
  - b) añade "$(=T$ si $\|f\|_\infty=0)$" y "única solución en todo $[t_0,t_0+\delta]$, $\delta\in(0,\delta_0]$";
  - la construcción de $F$ y $(P_F)$ pasa del enunciado a la demostración.
- Se mantienen las **3 etapas** del profesor:
  - **Etapa 1**: $F$, 3 casos, $(P_F)$ y continuidad, que da el apartado a);
  - **Etapa 2**: unicidad;
  - **Etapa 3**: existencia en $[t_0,t_0+\delta_0]$.
- Dentro de las etapas solo se corrige: se quita de la Etapa 1 el razonamiento circular y el párrafo de unicidad duplicado (eso es la Etapa 2); $M$ pasa a $\|f\|_\infty$; $F$ y $(P_F)$ pasan del enunciado a la Etapa 1.
- Errores corregidos:
  - en la Etapa 2 se usaba $\|\cdot\|_1$ en vez de $\|\cdot\|_2$;
  - no se explicaba por qué $t_1\ge t_0+\delta_0$ es contradicción ($t_1<\tilde t\le t_0+\delta_0$);
  - en la Etapa 3 se mezclaban $u$ y $U$;
  - el dibujo de la norma 1 etiquetaba el centro como $u(\tilde t)$ en vez de $u_0$; ahora va como observación;
  - había un párrafo de unicidad duplicado y un razonamiento circular ("asumiendo que la solución se mantiene en la bola").

### Teorema de unicidad global ✅
- $\tilde t\in(t_0,t_0+h]$ (antes $[t_0,t_0+h)$).
- Se justifica la cota de $D$: $\delta<\tilde t-t_0\le h$.
- Se justifica que $t_0+\delta^*<\tilde t$, necesario para poder plantear $(P^*)$, y que el $\delta$ de $(P^*)$ cumpla $t_0^*+\delta\le\tilde t$.
- Final como en clase: $\delta^*=\sup D\ge\delta^*+\delta$, absurdo (antes "$\delta^*\neq\sup D$ !!").
- Errata de LaTeX: en $(P^*)$ faltaba el salto de línea entre la ecuación y el dato inicial.

### Inicio de la demostración del 4º TF ✅
- $\Sigma$ con $I=[t_0,t_0+h)$ o $[t_0,t_0+h]$ y $u_I\in C^1(I;\overline\Omega)$.
- $\Sigma\neq\emptyset$ por C-L local aplicado a $f$ en $J\times\Omega$ ($u_0\in\Omega$ abierto).
- Se explica **para qué** se extiende $f$: como $\overline\Omega$ es cerrado, no se puede usar directamente la unicidad global. Cada solución local resuelve $(P_F)$, que tiene solución única (C-L global), así que dos soluciones locales coinciden y $u_{\max}$ está bien definida.
- Fórmula explícita de $F$ "por los rayos": $F(t,u)=f\big(t,q+R\frac{u-q}{\|u-q\|_2}\big)$ fuera de la bola.
