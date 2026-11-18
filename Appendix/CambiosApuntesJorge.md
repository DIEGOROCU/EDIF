# Cambios a partir de los apuntes de Jorge (16/11)

Comparación de nuestros `.tex` con las fotos de los apuntes de Jorge (12 fotos):
- Ascoli-Arzelà (págs. 1-2).
- Ejemplo $u''=u^4$ (págs. 1 y 3; **falta la pág. 2 en el zip**).
- Teoremas fundamentales 1º-4º, "mirar al pasado", logística y Volterra-Lotka (págs. 1-8).

Criterio: **añadir** siempre que se pueda; no se borra nada nuestro.

Leyenda: `[+]` se añade · `[~]` se corrige (errata o redacción)

---

## Theory/1 - Sistemas lineales generales Teoría general.tex

### Primer teorema fundamental
- [~] Errata: "En cuto caso" → "En cuyo caso".
- [+] Observación:
  - se está usando la norma $\|u\|_1=|u_1|+\dots+|u_N|$;
  - para $N=2$, que $|u_1|+|u_2|$ explote **no** implica que exploten ambas componentes: puede ser $|u_1(t)|\le C$ en $I$ y $\varlimsup|u_2(t)|=+\infty$.

### Tercer teorema fundamental
- [+] En la prueba de que $I\neq[t_0,T_{\max}]$: se explica que funciona porque $u(T_{\max})=u_1\in\Omega$ y se puede aplicar C-L local ("$u$ no puede acabar en un punto de $\Omega$").
- [+] "$\Gamma$ acotada $\Rightarrow\overline\Gamma$ **compacto** y $\overline\Gamma\subset\overline\Omega$". Se añade que $\Omega$ no tiene por qué ser acotado.
- [~] Errata en el dibujo del ejemplo: $u(t_n)\to u_\omega\in\Omega$ → $u_\omega\in\partial\Omega$.
- [+] Texto del ejemplo:
  - se ejemplifica la alternativa 2 con un $\Omega$ concreto (una franja);
  - las dos alternativas no son excluyentes;
  - $u_\omega$ **no tiene por qué ser único** ($\omega$-límites).

### Cuarto teorema fundamental
- [+] Enunciado: "da igual poner $\Omega$ que $\overline\Omega$" y "(si no, por C-L local se podría prolongar)"; $\partial\Omega=\partial B_R(q)$.
- [+] Comentario tras el enunciado: los cambios vienen de que ahora $f$ está definida en un **cerrado** (en toda la adherencia), no en un abierto.
- [+] Demostración:
  - la extensión de $f$ se hace "por los rayos" que salen de $q$;
  - "$(I_{\max},u_{\max})$ ya es la maximal, pero no hemos acabado";
  - si $T_{\max}=t_0+T$, ya $I_{\max}=J$.

### Mirar al pasado
- [+] Vale igual para $J=(-\infty,t_0]$.
- [+] Frase resumen de clase: un intervalo hacia la izquierda en el problema en $u$ equivale a uno hacia la derecha en el problema en $v$ ($s=2t_0-t$).

### Volterra-Lotka
- [+] Nota de notación: el profesor no usa $U=(u_1,u_2)$, $f=(f_1,f_2)$, sino $(u,v)$ y $(f,g)$.
- [~] Erratas:
  - $\|\frac{f_1}{\partial v}\|$ → $\left|\frac{\partial f_1}{\partial v}\right|$;
  - "FInalmente" → "Finalmente".

## Theory/2 - Ecuaciones no lineales de segundo orden.tex
- [~] Ejemplo $u''=u^4$: la existencia de la solución maximal se escribe con la cadena completa (C-L local → unicidad global → existencia y unicidad de solución maximal), como en clase.
- El resto del ejemplo ya estaba completo: energía, $T_{\max}$, simetría $w(t)=u(-t)$.

## Theory/3 - Teoría de Peano.tex
- Sin cambios. Ya estaba todo lo de Ascoli-Arzelà de Jorge:
  - ejemplo $x^n$;
  - definición de equicontinuidad;
  - lema de Lipschitz ⇒ equicontinua;
  - aplicación a sucesiones de soluciones;
  - demostración de $(1)\Rightarrow(2)$.

---

**Estado:** todos los cambios aplicados y compilados sin errores (16/11).
