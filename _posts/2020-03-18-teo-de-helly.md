---
layout: post
title: "Teorema de Helly."
mathjax: true
date: 2020-03-18
---



En esta pequeña entradita quiero dar una demostración de un teorema muy simpático y famosos de geometría convexa.
> #### Teorema de Helly.
> Sean $X_1, X_2, \dots X_n$ conjuntos cerrados y convexos de $\mathbb R^d$ tales que sus intersecciones de a grupos de tamaño $d+1$ son no triviales, entonces vale que, 
>  $\bigcap X_i \neq \emptyset$.

_Demo_: La idea es usar inducción en $n$ y en $d$. El caso básico de $d=1$ queda resuelto fácilmente. Supongamos que existe algún contraejemplo mínimo en $d$, con $n > d+1$ naturalmente. Lo que vamos a hacer pues es llegar a una contradicción de suponer que existen semejantes conjuntos.
Lo primero que hacemos es definir al conjunto $$Y_n= \bigcap_{i \neq n} X_i$$ tal que por como los tomamos deben ser que es disjunto de $X_n$ y es distinto de $\emptyset$ por ser mínimo.
Dado que ambos son cerrados disjuntos puedo considerarme el híperplano $H$ que los separa (este existe por una cuenta de cálculo avanzado no complicada). 
Sean ahora las proyecciones en el hiperplano para $i \le n-1$, $$Z_i = X_i \cap H$$ tales que son no nulas dado que los $X_i$ cumplen la propiedad Helly y que $Y_n$ es no vacío. Esto nos dice que la intersección al ser convexa y no vacía debe intersecar a $H$. Por lo tanto tenemos que los $Z_i$ cumplen la propiedad Helly pero por la minimalidad de $X_i$ debe ser que $$\bigcap Z_i \neq \emptyset$$
pero por otro lado tenemos que $$\bigcap Z_i = Y_n \cap H = \emptyset. $$ Llegamos así a una contradicción como queríamos ver. 




