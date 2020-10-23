---
layout: post
title: "Charlas septiembre-octubre 2020."
mathjax: true
date: 2020-23-10
---

Estos últimos meses estuve bastante asediado por la facultad y la vida pero aún así intenté ir a algunas charlas que me parecían interesantes. Estas son algunas de las charlas que asistí relativamente recientemente. Intenté plasmar lo que recordaba y lo que me interesó al escucharlas.

## Grupos y topología.

Charla del cibercoloquio de matemática. [Link](https://www.youtube.com/watch?v=CLvoiIzX5iE).

**Expositor.** Alejandro Adem.

**Resumen.** Estaba buena la charla porque arrancó con un problemita elemental de topología algebraica que es ver las acciones libres sobre esferas de dimensión par y de ahí fuimos generalizando e intentado responder el problema en su caso más general. 

**Apuntes.**

* Lo primero es medio pavo pero me gustó la manera en que se puede ver que si $G$ actua en $X$ debe ser que $|G| | \chi(X)$. Esto se debe a que la característica se separa para $\chi(X/G)$. Esto vale siempre que las cosas sean suficientemente buenas.

* Los primeros resultados que intentaron generalizar esto fueron efectivamente resultados que recuerdo haberme topado leyendo en la interné.

  * <u>Teorema (Smith)</u>. Si $G$ actua en $S^m$ entonces los subgrupos de $G$ son abelianos.
  * <u>Teorema (Milnor)</u>. Si $G$ actua en $S^m$ luego los elementos $g \in G$ tales que $o(g) = 2$ están en $ZG$ necesariamente.

* Otra dirección en la que se intentó generalizar es mirar $X \sim S^m$. Se obtiene un resultado muy similar al de Smith.

  * <u>Teorema(Swan)</u>. $G$ actua libremente en $X \sim S^m$ para algún $m > 0$  sii cada subgrupo abeliano de $G$ es cíclico.

* Finalmente llegamos a la dirección que tomó el autor de la charla. Acciones sobre productos de esferas. Consideramos las esferas homológicas racionales que son variedades tales que tenían la homología racional de la 3-esfera. Nos interesa las acciones que dan lugar a una acción trivial en homología. 

  *  En esta ámbito tiene sentido mirar acciones homotópicas que son lo que se imagina. Los resultados hoy en día son bastante técnicos y tenían muchas condiciones e hipotesis que olvidé.

    * Una acción homotópica era una de las clases de homotopía de las aplicaciones,

    $$
    f: BG \to BAut(X)
    $$

    ​	tal que la llamabamos una accion homotópica de $G$ en $X$.

  * Comentó otra manera de atacar estos problemas que es bastante algebraica. En sí me recuerda a cohomología de grupos. Bajo ciertas hipótesis nos construiamos un módulo $M_G(X)$ 

    * <u>Teorema (Wall) 1965</u>. Si veíamos que $M_G(X)$ era proyectivo esto nos decía que $G$ actuaba libremente en algún $Y$ de dimensión finita equivalente a $X$. 



## Operadas.

Charla del cibercoloquio de matemática. [Link.](https://www.youtube.com/watch?v=xNTjZIxz7UI)

**Expositora.** Ángelica Osorno.

**Resumen.** Siempre quise saber sobre operadas y la verdad es que me fascinó la idea del tema. Me gusta porque es álgebra con un feel diagramístico, ambas cosas que me interesan y sobre todo cuando se juntan. 

**Apuntes.**

* Arrancamos viendo todo en el espacio de loops $(\Omega(X), *)$ tal que no tiene asociativo ni elemento unidad salvo homotopía.

  * Viendo todas las maneras que tenemos de concatenar algunos caminos tenemos que dependiendo como pongamos los paréntesis tenemos tantas como número Catalan de cantidad de puntos tengamos.

* Una *operada* $\cal O$ es 

  * una flia de objetos indexada en los naturales. 

  * en cada ${\cal O}(k)$ actua el grupo $S_k$. 

  * un elemento inicial que es el $1$.

  * un colección morfismos entre estos objetos dadas de la sig manera,
    $$
    \gamma: {\cal O}(k) \times {\cal O}(j_1) \times \dots \times {\cal O}(j_k) \to {\cal O}(j_1 + \dots j_k)
    $$
    que cumplen algunos axiomas

* Algunos ejemplos son 

  *  ${\cal O} = End(X)$ para un cierto $X$. Donde $End(X)(k) = \{  f:X^k \to X \}$ continuas.
  * $Comm(k) = * $
  * $Assoc(k) = S_k$
  * Operados de n-cubitos. Donde $\cal C_n(k)$ son $k$  $n$-cubos con imagenes de los interiores disjuntas. Abajo tenemos $\cal C_2(5)$ por ejemplo.
    <img src="/home/emi/Documents/PINO/leolerena.github.io/fotos/5b58d59918120c8a9d538252_2cube.jpg" alt="What is an Operad? Part 2" style="zoom: 50%;" />

* La manera de representarlas es como árboles donde las ramas corresponden a los morfismos que salen de cada objeto.

  

## Potencias n-ésimas en grupos libres.

Charla de UMA.

**Expositor.** Jonathan Barmak.

**Resumen.** Fue una charla de trabajo reciente sobre algunos problemas de teoría de grupos. Si mal no recuerdo la idea era tomar para el grupo libre en dos generadores, por ejemplo, las palabras que se pueden formar pensadas como curvas. La idea era trabajar combinátoricamente con estas curvas e intentar deducir cualidades del grupo en cuestión. Recuerdo que nos preocupabamos por los ciclos que se podían formar y por aproximar curvas de este estilo por poligonales buenas.

**Apuntes.**

* El siguiente resultado sobre palabras en $\Bbb F_2$.
  * <u>Teorema (Lydon-Newman) 1973</u>: $[x,y]$ es producto de 3 cuadrados pero no de 2 cuadrados en $\Bbb F_2$.
* Aprendí de otras familias de grupos que parecen clásicos e interesantes. 
  * Los grupos metabelianos que son tales que su conmutador son abelianos.
  * Los grupos de Burnside son grupos que están parametrizados por dos naturales. Entonces el grupo $B(m,n)$ es el grupo en $m$ generadores y con la relación $x_i^n = 1$ para cada $i=1 \dots m$. 
    * Un problema histórico es ver para qué valores son grupos finitos.
* El medallista Fields <u>Zelmanov</u> recibió la medalla fields por su trabajo en este campo si bien su enfoque tengo entendido vino más por el lado de los grupos de Lie.



