---
layout: post
title: "Teorema central del límite."
mathjax: true
date: 2020-03-07
---


Recién ayer pude dar el final de proba. Pasaron dos añitos de aquella cursada. Para festejar voy a escribir un poquito sobre el teorema central del límite que es uno de los resultados más importantes de la teoría de la probabilidad.

### Enunciado del teorema central del límite.

El teorema se puede enunciar de dos maneras dependiendo qué herramientas tengamos para demostrarlo. En el caso más usual se enuncia como,
> *Teorema Central del límite:* Sean $(X_n)$ variables aleatorias con esperanza finita, varianza finita y tercer momento finito. Entonces la variable aleatoria $Z_n = \dfrac{\sqrt{n}}{\sigma^2}{\overline{X}_n}$ converge en distribución a una variable aleatoria con distribución $N(0,1)$.

Donde la hipótesis de tercer momento finito se puede omitir si sabemos usar las funciones características. En tal caso la demostración pasa a ser más directa pero primero habría que demostrar algunos resultados no triviales como el teorema de Lévy. 

### ¿Por qué el enunciado es así?
Es medio extraño todo el enunciado sin aclarar mucho por qué lo estamos haciendo. La verdad es que si sabemos la ley de los grandes números sabemos que toda sucesión de variables aleatorias promediadas convergen a la esperanza de ellas. En este caso lo que estamos haciendo es multiplicar por la raíz de $n$ porque ese es el orden de convergencia para que en este caso converja a una variable aleatoria. Dividimos por la varianza para que nos quede algo de varianza exactamente $1$. 

El porqué converge a una normal está dado porque la distribución de $Z_n$ es simétrica respecto al $0$ y cumple algunas propiedades que terminan caracterizando a las distribuciones normales. Esto nos da una sugerencia que debe converger a una normal.

El primero en darse cuenta de este fenómeno fue el fenómeno de _Abraham de Moivre_ en el siglo XVIII. Se fijó en el caso básico de una Bernouilli de paramétro $(1/2)$. Los siguientes histogramas nos permiten visualizar esta convergencia a medida que aumentamos la cantidad de muestras.

![alt text](https://i.stack.imgur.com/wPGzI.png "Logo Title Text 1")

### ¿Por qué no se puede pedir aún menos?
Veamos que no se puede sacar ninguna hipótesis. En particular si el segundo momento no es finito y converge a una normal dado que la normal siempre tiene varianza finita (es el segundo paramétro) debe ser que no puede converger a una normal. El caso más ilustrativo es el de la distribución de Cauchy $C(0,1)$ tal que no tiene esperanza y claramente no tiene segundo momento finito. Con un poco de análisis complejo se puede ver que su función característica es $e^{-|t|}$, y haciendo una simple cuenta podemos ver que $Z_n$ tiene distribución $C(0,1)$ por lo tanto no puede converger nunca a una normal.

### Referencias:
* [Cauchy Distribution and Central Limit Theorem](https://stats.stackexchange.com/questions/74268/cauchy-distribution-and-central-limit-theorem)
* [What intuitive explanation is there for the central limit theorem?](https://stats.stackexchange.com/questions/3734/what-intuitive-explanation-is-there-for-the-central-limit-theorem/3904#3904)

