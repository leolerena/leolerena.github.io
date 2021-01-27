---
layout: post
title: "Teorema de Helly."
mathjax: true
date: 2020-03-18
---



En esta pequeña entradita quiero dar una demostración de un teorema muy simpático y famoso de geometría convexa.
> ### Teorema de Helly.
> Sean $X_1, X_2, \dots X_n$ conjuntos cerrados y convexos de $\mathbb R^d$ tales que sus intersecciones de a grupos de tamaño $d+1$ son no triviales, entonces vale que, 
>  $\bigcap X_i \neq \emptyset$.

_Demo_: La idea es usar inducción en $n$ y en $d$. El caso básico de $d=1$ queda resuelto fácilmente. Supongamos que existe algún contraejemplo mínimo en $d$, con $n > d+1$ naturalmente. Lo que vamos a hacer pues es llegar a una contradicción de suponer que existen semejantes conjuntos.

Lo primero que hacemos es definir al conjunto $$Y_n= \bigcap_{i \neq n} X_i$$ tal que por como los tomamos deben ser que es disjunto de $X_n$ y es distinto de $\emptyset$ por ser mínimo.
Dado que ambos son cerrados disjuntos puedo considerarme el híperplano $H$ que los separa (este existe porque son cerrados por hipótesis). 

Sean ahora las proyecciones en el hiperplano para $i \le n-1$, $$Z_i = X_i \cap H$$ tales que son no nulas dado que los $X_i$ cumplen la propiedad Helly y que $Y_n$ es no vacío. Esto nos dice que la intersección al ser convexa y no vacía debe intersecar a $H$. Por lo tanto tenemos que los $Z_i$ cumplen la propiedad Helly pero por la minimalidad de $X_i$ debe ser que $$\bigcap Z_i \neq \emptyset$$
pero por otro lado tenemos que $$\bigcap Z_i = Y_n \cap H = \emptyset. $$ Llegamos así a una contradicción como queríamos ver. 

### Chequeo de hipótesis.
Veamos en esta sección que no podemos sacar ninguna de las hipótesis. Si cambiamos la condición Helly para verificar intersecciones de $d$ elementos el contraejemplo que nos podemos armar son tres rectas tales que sus intersecciones de a pares formen un triangulo no trivial. Si en cambio sacamos la condición de convexidad podemos hacernos facilmente varios ejemplos no conexos pero si mantenemos la conexión nos alcanza con tomar en el plano el borde de un cuadrado y por cada vértice tomar los dos ejes contiguos más un poquito de los otros dos ejes. De esta manera es fácil ver que cumple que toda intersección de a triples es no nula pero sí lo es la intersección de los 4 subconjuntos.



