# Representación y función de Green.

## Introducción

Sea $U$ abierto de $\Bbb R^n$, consideremos el problema de Poisson, es decir la siguiente ecuación diferencial para una función $f \in C^2_c(U)$

$$-\Delta u = f $$
que sabemos que su solución está dada por la siguiente función $u=\phi * f$. Por las propiedades de la convolución como $f$ es acotada por suposición tenemos que $u$ es acotada. Por otro lado pensemos que existe otra función $v$ que resuelve el problema y **también es acotada**. Por el teorema de Liouville como 
$$\Delta (u-v) = 0 $$
y es acotada esa diferencia debe ser que $u-v$ es constante. 

Ahora usemos la fórmula de Green para $u,v$ recordemos que en cierta manera es la generalización de integrar por partes entonces nos queda lo siguiente para $n$ normal,
$$\int_U \Delta u v - u\Delta v = \int_{\partial U} \partial_nuv -   u\partial_nv  dS$$

## Qué intentamos resolver?

Queremos tener una fórmula para $u(x)$ en un punto $x \in U$ que dependa  solo del laplaciano $\Delta u$ y de los valores que toma la función en el borde. Resolviendo este problema vamos a toparnos con una función que aparece en esta fórmula que vamos a llamar función de Green.


## Cómo lo resolvemos?



La idea ahora es considerar una bola $B_\epsilon(x) \subset U$ y ahora miramos el dominio dado por $U \setminus B_\epsilon(x)$ y en este dominio aplicamos Green para la función $u$ y la función 
$$ v(y) = \phi(x-y). $$

Sabemos que la función $v$ así definida es armónica dado que resuelve la ecuación de Laplace. Lo que nos interesa ahora es notar que para Green nos queda lo siguiente

$$\int_U \Delta u v  = \int_{\partial U} \partial_nuv -   u\partial_nv \quad  dS - \int_{\partial B_\epsilon(x)} \partial_nuv -   u\partial_nv \quad dS$$

el signo menos aparece porque esta integral en el borde de la bola tiene la otra normal apuntando para adentro. 

Lo que hacemos es tender $\epsilon \to 0$ y ver que el término del borde
$$\int_{\partial B_\epsilon(x)} \partial_nuv  \to 0$$
 por otro lado la otra parte del borde de la bola es tal que nos queda la siguiente expresión
 $$\partial_n v = \dfrac{1}{n\epsilon^{n-1}\omega_n } $$
 que mágicamente transforma la integral del borde tomando límite en $\epsilon$ en 
 $$\int_{\partial B_\epsilon(x)}   u\partial_nv dS \to  u(x).$$

Entonces es buenísimo porque ahora podemos representar a $u(x)$ por medio de unas integrales en el borde,
$$ u(x) =  \int_U \Delta u v  - \int_{\partial U} (\partial_nuv -   u\partial_nv)   dS $$

Esta fórmula es muy simpática porque en cierta manera nos dice que podemos recuperar el valor de $u$ conociendo su laplaciano y su valor en el borde del mismo. Podemos ser más ambicioses e intentar sacarnos de encima esta normal $n$. Para eso consideremos la función auxiliar que resuelva la siguiente ecuación en $U$
$$\Delta \varphi_x = 0  $$
y que en el borde $\partial U$ valga que 
$$ \varphi_x(y) = \phi(x,y) $$
Si hacemos Green tal como hicimos antes lo que podemos notar es que en este caso nos queda que
$$ \int_U \Delta u \varphi_x(y)  = \int_{\partial U} (\partial_nu\varphi_x -   u\partial_n\varphi_x)dS $$
y usando que sobre el borde $\partial U$ las funciones $\varphi_x(y) = \phi(x,y)$ por como mismo la definimos tenemos que en ese caso si consideramos la función 
$$G(x,y) =\phi(x,y) - \varphi_x(y)$$
que llamaremos **función de Green** de manera que si reemplazamos en la ecuación antes dado nos queda la siguiente igualdad muy simpática
$$ u(x) =  \int_U \Delta u G(x,y)  - \int_{\partial U}   u\partial_nG(x,y)  dS. $$

Con esto estamos satisfechos porque resolvimos el problema que habíamos planteado.



---



