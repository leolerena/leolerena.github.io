---
layout: post
title: "Teorema de Hall para matchings y algunas aplicaciones."
mathjax: true
date: 2020-01-09
---

Ultimamente estuve intentando ponerme al tanto con algunos resultados básicos de teoría de grafos clásica para poder usarlos más en adelante y no tener tanto miedo. La exposición es poco detallada.

Sea $G$ un grafo _finito_ bipartito, tal que ambas particiones $A, B$ tienen la misma cardinalidad.

 
 **Teorema de Hall para grafos bipartitos.** La partición $A$ tiene un matching sii para todo subconjunto de vértices $S$ de $A$ resulta que $|N(S)| \ge |S|$.

Existen muchas demostraciones posibles, por ejemplo usando el teorema de König o los augmenting path, que son caminos que te permiten aumentar el tamaño del matching.

Lo que me pareció muy divertida fue la siguiente demostración de un resultado clásico usando este teorema (que en principio no me pareció tan wow, pero es uno de los resultados más aplicados de toda la teoría de grafos). Recordemos que un $k$-factor es un subgrafo que es $k$-regular.


![https://user-images.githubusercontent.com/31391855/105626531-05d07500-5e0f-11eb-8286-631e29fe756a.png]



 **Teorema de Petersen.** Todo grafo $2k$-regular tiene un 2-factor.

_Demostración_: Como queremos usar el teorema de Hall necesitamos armarnos un grafo bipartito. Para eso usamos estos dos resultados clásicos de teoría de grafos. 
El primero es que todo grafo de grado par tiene un camino de Euler. El segundo resultado es que todo grafo bipartito $k$-regular tiene un matching (esto es chequear la _marriage condition_). 
Para usar estos resultados consideremos el grafo que se obtiene de agregar dos vértices, $v^{+}, v^{-}$ por cada vértice de $G$, y agregar la arista $v_{i}^{+} v_{i+1}^{-}$ por cada arista $v_i v_{i+1}$ del camino de Euler. Este nuevo grafo que nos armamos es bipartito y $k-$regular, por lo tanto tiene un matching que es un 1-factor. Juntando los dos vértices en uno solo tenemos entonces un 2-factor como buscábamos.
$$\tag*{$\blacksquare$}$$

Esta demostración me pareció muy simpática porque nos estamos construyendo otro grafo básicamente y agregando una copia extra por cada vértice. Me recuerde de manera muy vaga al revestimiento de orientaciones de dos hojas y a la demo para ver que es orientable.
 
**Referencia:** Diestel, _Graph Theory_
