---
layout: post
title: "Dudas acumuladas."
mathjax: true
date: 2020-03-14
---


## Sugerencias - Ej 16 - Práctica 4. 

![image-20200521191732463](/home/emi/.config/Typora/typora-user-images/image-20200521191732463.png)

<img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.pinimg.com%2F736x%2F06%2F8e%2Fe5%2F068ee506fe11c524d94c9e83d88ea4c3--maths-geometry.jpg&amp;f=1&amp;nofb=1" alt="Cylinder - 3D Shape - Geometry - Nets of Solids ..." style="zoom:55%;" />

## Idea.

La idea es usar teo de div (Gauss). Notemos que en particular $div(F)=0$ . Esto nos dice que si miramos la integral sobre una superficie $S$ que es cerrada resulta ser que 
$$
\int_S F dS = 0.
$$
Notemos que en particular la normal sobre el cilindro (en el borde) es de la siguiente forma:
$$
T_t \times T_z = (x(t),y(t),0)
$$
para eso hagan la cuenta con cilíndricas. Esto nos dice entonces que si queremos calcular la integral del volumen encerrado entre las dos secciones oblicuas dado que sobre las "paredcitas" del cilindro la normal mata al término $z$ entonces nos queda que 
$$
\begin{align}
\int_{S_1} F dS + \int_{S_2} F dS + \int_{B} F dS &= 0  \\
\int_{S_1} F dS  &= - \int_{S_2} F dS
\end{align}
$$
si todos están con la misma orientación. Entonces nos basta con calcular sobre una sola sección oblicua. 

Para terminar el ej veamos de resolver el ítem b) así de paso obtenemos sin hacer toda la cuenta el ítem a).

Escribamos la intersección. $$x^2 + y^2 \le a^2$$ para $D=\{(x,y,z) \ | \ z=0 \}$ , es el disco de radio $a$ centrado en el $(0,0,0)$ con la normal que apunta para arriba del plano  y que apunta al interior del cilindro.  Entonces nos queda la siguiente integral,
$$
\int_{S_1} \langle F, N \rangle dS = \iint_{D} a^2 - x^2 - y^2 \ dx \ dy
$$
que pasando a polares es bastante tranqui 
$$
\int_{0}^{a^2} \int_{0}^{2\pi} (a^2 - r^2)r \ d\theta \ dr = \int_{0}^{a^2} 2\pi (a^2 - r^2)r \ dr =^{?} \text{ALGO}
$$

## Respuesta

¿Dépende el flujo del área?

NO!!

No importa cual sea el área de la sección oblicua dado que usando el teo de Gauss podemos ver que es igual a la integral de cualquier otra sección oblicua de area arbitraria.

