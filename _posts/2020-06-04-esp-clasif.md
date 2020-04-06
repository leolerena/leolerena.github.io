---
layout: post
title: "Una construcción de los espacios clasificantes."
mathjax: true
date: 2020-04-06
---

Antes que nada quiero decir que estas notas las había tomado cuando estaba cursando topología algebraica allá un año atrás cuando aún eramos libres de ir a la facultad. Pienso subir algunos otros apuntes misceláneos que tengo por ahí dando vuelta en la pc por lo menos para que estén en algún lugar con posibilidad (remota) de ser útiles para alguien. 

------------------------------
Estos son espacios que su tipo homotópico depende exclusivamente de su grupo fundamental. Esto es que si $X$ es $K(G,1)$ luego su grupo fundamental $\pi_1 X=G$ y los demás grupos de homotopía son nulos. Además pediremos que sea un CW complejo conexo para tener resultados de clasificación más simpáticos.

**Una construcción de $K(G,1)$ usando espacio clasificante.**

El primer ejemplo que viene a la cabeza es el de $S^1$ que resulta ser un $K(\mathbb Z,1)$. ¿Cómo podemos extender este resultado para grupos abelianos finitamente generados? Pensemos en un grafo $X$ que sabemos que tiene grupo fundamental generado por los ciclos que resulta ser $G$ un grupo libre. Su revestimiento debe ser un grafo pero simplemente conexo. Esto es que su revestimiento sea un árbol, equivalentemente. Dado que es un CW complejo de dimensión 1, sus grupos de homotopía mayores son todos nulos. Recordemos que estos grupos de homotopía son isomorfos con los grupos de homotopía del grafo. Concluimos entonces que $X$ es un $K(G,1)$.

Ahora que sabemos como obtener los $K(G,1)$ correspondientes a grupos libres, veamos de extenderlo a todos los grupos. Como esto no es tan evidente, recordemos un ejemplo y veamos de entender como construirlo de esta manera.

Sabemos que el CW complejo $S^{\infty}$ resulta ser un revestimiento del CW complejo $\mathbb{RP}^{\infty}$. Esto se puede ver porque cada $S^n$ es un revestimiento respectivamente del $\mathbb{RP}^n$ . El CW complejo $S^{\infty} $ es un espacio contractil dado que todo mapa de $S^n$ lo podemos ver que cae dentro de $S^{n+1}$, de manera que es nulhomotópico. Esto quiere decir que $S^{\infty}$ es contractil y por lo tanto el revestimiento universal de $\mathbb{RP}^{\infty}$. De esta manera vimos que $\mathbb{RP}^{\infty}$ tiene todos los grupos de homotopía nulos salvo el primero que resulta ser $\mathbb Z_2$. Para ver esto notemos que todo mapa $f:S^1 \to \mathbb{RP}^{\infty}$ cae dentro de algún $\mathbb{RP}^n$. Dado que para $n>1$ todos los $\pi_1$ de los espacios proyectivos $\mathbb{RP}^n$ son exactamente $\mathbb Z_2$, concluimos que 
$$\pi_1 \mathbb{RP}^{\infty} = \mathbb Z_2$$ por lo que $\mathbb{RP}^{\infty}$ es un $K(\mathbb Z_2, 1)$.
_Como curiosidad este mismo ejemplo sirve para ver que no todo revestimiento universal de un CW complejo es un revestimiento universal en cada celda del complejo._

¿Cómo podemos entonces obtener $K(\mathbb Z_n,1)$ para $n\in \mathbb N$ arbitrario? En el caso anterior fuimos construyendo un revestimiento para cada espacio proyectivo que es un cociente de la esfera por medio de la acción de $G_2$. El problema ahora es que para un $n \in \mathbb N$ arbitrario no podemos hacer esto, dado que sobre las esferas de dimensión par solo puede actuar libremente $G_2$ sobre ellas. Lo que podemos hacer entonces es fijarnos en el espacio total $S^{\infty}$ y ver la acción de $G_n$ sobre él. Esto nos va a dar un revestimiento de la esfera infinita en este cociente. En definitiva aún no tenemos las herramientas para hacerlo de esta manera, pero usando el siguiente resultado queda claro como construirlo.
> **Teorema.**
	Si $G$ actúa libremente y de manera propiamente discontinua sobre un espacio contráctil $\operatorname{EG}$, luego resulta que $EG/G$ es un $K(G,1)$.


Si nos creemos esto por ahora tenemos una manera de construir espacios $K(G,1)$ para grupos $G$ finitamente generados. O sea ya sabemos construir los grupos de torsión y los libres. Nos falta poder tomar un producto entre ellos. Para eso lo más natural funciona y esto es que 
$$
K(G \times H,1) = K(G,1) \times K(H,1)
$$
esto sale de que el revestimiento de un producto resulta ser el producto de los revestimientos y que el producto se lleva bien con el grupo fundamental.

Ya medio que estamos en condiciones de construir un $K(G,1)$ para un grupo $G$ arbitrario. La construcción es particularmente interesante porque vamos a construir un CW complejo a partir de un grupo. Consideramos un complejo con n-símplices dados por las (n+1) tuplas ordenadas como $[g_0, \dots, g_n]$. Esta construcción tiene lo interesante que es contractil, por ejemplo, podemos ver que todo punto que está en el interior de un símplex $[g_0, \dots, g_n]$ lo podemos llevar por una homotopía al punto $e$ en el simplex $[e,g_0, \dots, g_n]$. De esta manera vemos que EG se trata de un espacio contractil. Esto se debió a que tenemos infinitos símplices pero con la cualidad que para cada símplex existe uno de dimensión superior que contenga a cualquier elemento arbitrario (en este caso en particular usamos $e$ pero bien podríamos haber usado otro elemento del grupo $G$).

Esperaríamos que este espacio $EG$ tenga una buena relación con el grupo $G$ y de hecho la tiene. Se puede ver directamente que actúa a izquierda de manera libre puesto que $ge=e$ solo cuando $g=e$. Ahora con un esfuerzo podemos ver la siguiente proposición.
> **Proposición.**
	El mapa cociente $q:EG \to EG/G$ es un revestimiento.
	
Llamaremos al espacio cociente por el nombre $BG \coloneqq EG/G$. Resulta que $EG$ al ser contractil, va a ser el revestimiento universal de $BG$. Si consideramos el siguiente teorema no trivial.
> Teorema.
> Dado un revestimiento universal del tipo $q:EG \to EG/G$ resulta que $\operatorname{Deck}(q)=G=\pi_1(BG)$.

Obtuvimos que $BG$ va a ser un espacio con grupos de homotopía triviales para $n>2$ y grupo fundamental exactamente $G$ por construcción. Esto no nos dice que sea un $K(G,1)$. Si bien es claro que es conexo, no es tan claro que sea un CW complejo. Para eso veamos cómo son los símplices en este cociente. Notemos que para todo símplex en EG lo podemos escribir de esta manera
$$
[g_0,g_0g_1, \dots, g_0g_1 \dots g_n] = g_0 [e,g_1, \dots, g_1 \dots g_n]
$$
 y así podemos escribir de manera única a la imagen de este simplex en $BG$ de la siguiente manera $$[g_1 | \dots | g_n].$$ Los símplices que están en su borde son los que son del tipo $[g_2| \dots| g_n], [g_1| \dots| g_{n-1}]$ y los del tipo $[g_0| \dots| g_ig_{i+1}|\dots| g_n]$ para $1<i<n$. Podemos ver que estos son símplices si lo mirás como su representante en EG y ahí recordás que sus caras son símplices que le faltan alguno de los $g_i$ de la tira del simplex del cual son una cara.


Ya tenemos construidos los espacios $K(G,1)$, nos gustaría saber qué relación hay entre ellos. Es decir dados dos espacios de la familia de espacios $K(G,1)$, ¿qué tienen en común? El siguiente resultado es super importante, ya que nos dice que estos espacios son todos homotópicamente equivalentes. Esto medio que lo podríamos intuir dado que tienen los mismos grupos de homotopía y quizá por Whitehead podríamos ver que son homotópicamente equivalentes. El problema es que para usar Whitehead necesitamos que los isomorfismos inducidos en los grupos homotópicos provengan de una misma función y esto no es nada trivial de hacer para espacios genéricos. Aún así tenemos una pequeña esperanza dado que solo hay un grupo de homotopía no trivial. En particular podemos ver que vale la siguiente proposición que esconde la dificultad de este resultado.

> **Proposición.**
	Sea $(X,x_0)$ un CW complejo, $Y$ un $K(G,1)$ luego todo morfismo 
	\[\phi:\pi_1(X) \to G\]
	 se realiza como el inducido por una función continua $f:X \to Y$.


Suponiendo que vale la proposición no queda más que usarla y junto con el teorema de Whitehead deducir que todos los $K(G,1)$ son homotópicamente equivalentes.

-----------------------------
**Referencia.** 
* Hatcher, _Algebraic topology_.


