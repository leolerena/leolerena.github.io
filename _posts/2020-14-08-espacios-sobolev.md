---
layout: post
title: "Espacios de Sobolev."
mathjax: true
date: 2020-08-15
---



## ¿Qué son?

La idea es cambiar el foco y mirar un espacio distinto al que veníamos trabajando. Lo que vamos a hacer es mirar un subespacio de $L^2$. Esto es vamos a tomar las siguientes funciones,
$$H^1(U) = \{ v \in L^2(U) | \partial_1 v, \dots, \partial_nv \in L^2(U) \}$$
donde las derivadas las estamos pensando en el sentido de una distribución. Recordemos que para hacerlas en este sentido lo que hacemos es pasarle la derivada a una función test. Este primer espacio resulta ser un espacio de Sobolev, pero no es el único. Vamos a tener las siguientes variaciones,

-  $v \in L^p(U)$ para $p \in (1, \infty)$
-  $\partial_{\alpha} v$ para $\alpha$ de longitud $\le n$ arbitraria

En otras palabras podemos mirar las derivadas del orden que querramos que estén en  el espacio que querramos. Estos espacios los denotaremos $W^{k,p}$ genéricamente y su definicón es la siguiente,

![image](https://user-images.githubusercontent.com/31391855/90304465-a6992c80-de8e-11ea-98aa-ce87d0806b41.png)

 Notemos que $H^1(U)$ es $W^{1,2}$ siguiendo esta notación. Este espacio tiene la ventaja aparte de ser un **espacio de hilbert**, es decir que por medio del producto interno 

![image](https://user-images.githubusercontent.com/31391855/90304657-68047180-de90-11ea-8d5e-c51b9590aeea.png)

es un espacio normado y métrico y podemos ver que es completo. Esto es algo excelente para nosotres dado que entra en juego todos los resultados de análisis funcional que ya teníamos. 

Un espacio que nos va a interesar que es similar a este es 

![image](https://user-images.githubusercontent.com/31391855/90304676-93875c00-de90-11ea-9231-f2855b2b14ef.png)

que podemos pensar como las funciones de soporte (*no necesariamente*)compacto en $U$ tales que estám en $H^1$. No van a seguir teniendo soporte compacto pero seguro que valen 0 en $\partial U$. Nuestros objetivos van a ser los siguientes,

1. Estudiar estos espacios en líneas más a lo análisis funcional e intentando entender su topología.
2. Plantear formulaciones débiles de algunos problemas y resolverlos en estos espacios.
3. Ver que hay una base de $H^{1}_0(U)$ formada por autofunciones de $-\Delta$.



## Estructura de los espacios de Sobolev.

Es un espacio que tiene muchas cosas lindas y feas a la vez tal como $L^2(U)$. Las funciones infinitamente diferenciables de soporte compacto están contenidas en este espacio pero así también algunos casos más patológicos como funciones que no son acotadas en ningún abierto de $U$. Lo que hacemos entonces es intentar ver resultados de densidad para ver de qué realmente *está hecho el espacio.* 



Lo primero es notar que como espacio $W^{k,p}(U)$ tiene las siguientes características muy copadas:

1. Es un **Banach** (espacio vectorial completo) para $p \ge 1$.
2. Es **separable**, por lo que  tiene una base contable de abiertos. Esto es un pasito antes de ser compacto. Vale para todo $1\le p<\infty$.
3. Es **reflexivo**, por lo que es isomorfo como espacio normado a su doble dual por medio del mapa de evaluación. Esto vale para $1<p<\infty$.

Por medio de estas propiedades podemos ver algunos resultaditos que cumplen las funciones de estos espacios, en general vale lo siguiente,

![image](https://user-images.githubusercontent.com/31391855/90304688-aa2db300-de90-11ea-9f49-d628b8f52f40.png)

que nos dice que el gradiente es cero sii u es constante y que se lleva bien con partes positivas, negativas y así con los módulos.

### Convergencia y densidad.

Pasemos ahora a mirar qué pasa cuando miramos sucesiones en estos espacios y cómo son las convergencias acá. Por un lado tenemos un resultado medio Riemann-Lebesgue salvador que es el siguiente,

![image](https://user-images.githubusercontent.com/31391855/90304697-bca7ec80-de90-11ea-8284-fdde24fe2ce1.png)


tal que nos dice que es denso con la topología del espacio de Sobolev, esto es big news y super util. Tengamos en cuenta que no vale para funciones con soporte compacto. La razón cae en que no le pedimos nada a nuestro conjunto $U$. Si le pedimos un poquito más de regularidad obtenemos el siguiente resultado,

![image](https://user-images.githubusercontent.com/31391855/90304705-cdf0f900-de90-11ea-99c3-aeba7dd364cc.png)

que es una gran mejora pero hay que garantizar que el borde sea $C^1$ y esto es que sea la imagen de una función $C^1$ por medio del teo de función implícita.



Otro resultado interesante y útil va a ser un análogo del teorema de Arzela-Ascoli. Es decir un teorema que nos va a decir cuando una existe una sub-sub sucesión que converge a una función. Para esto vamos a pedirle algunas cositas al abierto $U$, de nuevo el enunciado de **Rendrich-Kondrakov(R-K)** es el siguiente,

![image](https://user-images.githubusercontent.com/31391855/90304708-db0de800-de90-11ea-9d59-c3688fa814a4.png)

que notemos no es una convergencia fuerte sino que débil pero viene con yapa. Es decir viene con convergencia en $L^p$ y con un control de estabilidad para el gradiente. Está bueno pensar contraejemplos para los siguientes casos ([ver teórica sino](http://cms.dm.uba.ar/academico/materias/1ercuat2020/ecuaciones_diferenciales/Sobolev.pdf))

*  $U$ no es acotado.
*  Pedimos convergencia fuerte en $W^{1,p}(U)$ en vez de débil.

### Traza y $W_0^{1,p}$.

Pensemos que $U$ es un abierto acotado y nos gustaría dada $u \in W^{1,p}(U)$ definir su valor en el borde. En principio salvo que sea continua ahí nos va a quedar cualquier cosa horrible o incluso no va a estar definida. ¿Qué podemos hacer? Podemos considerar un operador que dada una función en el espacio de Sobolev nos devuelva alguien del borde que coincida con ésta en caso de estar definida. A esta función la llamaremos **traza** y sí, tiene una gran relación con la de álgebra lineal pero eso lo veremos más en adelante. Por ahora quedemonos con el siguiente resultado,

![image](https://user-images.githubusercontent.com/31391855/90304722-f24cd580-de90-11ea-8e56-9f6150e93dc8.png)

Esto está bueno porque nos permite retomar la idea que teníamos antes de $W_0^{1,p}(U)$ como las funciones que eran $0$ en el borde por ser límite de funciones de soporte compacto contenido en  $U.$ El siguiente resultado formaliza esta intuición,

![image](https://user-images.githubusercontent.com/31391855/90304732-ff69c480-de90-11ea-8346-853c3542f62c.png)


donde la condición de regularidad de $U$ se la pedimos para poder usar el resultado de R-K.

### Desigualdad de Poincaré y normas.

Esta desigualdad como todas las desigualdades en análisis son super utiles. En este caso nos va a permitir acotar por medio de una constante la norma en $L^p$ de una función de $W^{1,p}_0 (U)$ por la norma de su gradiente en $L^p$. Notemos que está bien definido por donde estamos mirando nuestro espacio. El enunciado es el siguiente,

![image](https://user-images.githubusercontent.com/31391855/90304743-114b6780-de91-11ea-9ae1-767fd97d9ce5.png)

y esto medio que parece algo curioso pero para qué sirve ¿¿??. Bueno, la respuesta es que nos permite ver que en este espacio las normas $$||\Delta u ||_p $$ y $$|| u ||_{W^{1,p}}$$ son equivalentes!! Es decir que siempre podemos encontrar una bola dentro de otra bola dada para ambas normas.

¿Por qué no podemos hacer esto en $W^{1,p}(U)$ ? 

La respuesta es que lamentablemente $||\Delta u ||_p$ no es una norma sino que una semi norma. Esto es porque las constantes tienen norma $0$ pero son diferentes entre sí. O sea la norma no separa a la función 0. Pero gracias al ingenio del análisis podemos hacer algo interesante y aún así usar esta norma para acotar la norma de $L^p$. Tenemos el siguiente resultado,

![image](https://user-images.githubusercontent.com/31391855/90304745-22947400-de91-11ea-9d3f-7820adb2f936.png)

donde notemos que el problema con las constantes ya no nos importa porque consideramos al promedio $\overline u$  sobre todo $U$ tal como hacíamos para las funciones armónicas. ~~En cierta manera estamos limpiando las constantes y las partes donde la función es localmente constante para ahí sí poder obtener una cota~~. Sino podemos sacar el promedio directamente y restarselo para tener una cota más limpia como en el segundo resultado.

### Derivadas fraccionarias.

Dado una función en $L^2(\Bbb R^n)$ nos gustaría poder considerar sus derivadas en sentido de dist dado que en principio no tienen derivadas así como así. Una vez que consideramos estas derivadas lo que hacemos es pensar si están ellas mismas en $L^2(\Bbb R^n)$ y esto lo podemos reescribir en términos de su transformada de Fourier. En definitiva nos termina quedando el siguiente espacio,

![image](https://user-images.githubusercontent.com/31391855/90304752-350ead80-de91-11ea-987a-8547d6906eec.png)

aparte tenemos un resultado de inmersión topológica como subespacio de estas funciones con derivadas fraccionarias en el espacio de funciones continuas. Este resultado nos dice que podemos mirar a estas funciones como un subespacio de las funciones

![image](https://user-images.githubusercontent.com/31391855/90340671-44484500-dfd0-11ea-802e-288b5919216d.png)



## Formulación débil de ecuaciones elípticas.

Consideremos uno de nuestros problemas preferidos de la materia, es decir la siguiente ecuación

$-\Nabla u = f, \ \ \text{en} \ \ U, u=0 \ \ \text{en} \ \partial U$
para un abierto acotado suave y una función $f \in L^2(U).$ Nuestra formulación débil corresponde a  hallar una función $u \in H_{0}^1(U)$ tal que 
$(u,v)_{H^1_0(U)} = (f,v)_{L^2(U)} \ \ \ \forall v \in H_0^1(U)$
y la existencia y unicidad la vamos a obtener del siguiente resultado de Riesz,

![image](https://user-images.githubusercontent.com/31391855/90304758-45bf2380-de91-11ea-9cd3-f4e86acc7ffb.png)


Este resultado aparecía en una guía de cálculo avanzado y creo que en lineal. Es el famoso teorema de representación de Riesz dado que a cada funcional $\phi$ lo estamos representando por un único $u$. A su vez tenemos la caracterización variacional que nos va a ser de gran utilidad a la hora tener cotas o controles sobre las normas.

### Condición de Neumann sobre el borde.

¿Qué pasa si ponemos una condición de Neumann sobre el borde? Es decir si pedimos algo así,
$$ -\Nabla u = f, \ \ \text{en} \ \ U, \partial_{\nu}u=0 \ \ \text{en} \ \partial U $$


en tal caso podemos usar las fórmulas de green para llevarlo al siguiente problema,

![image](https://user-images.githubusercontent.com/31391855/90340723-97ba9300-dfd0-11ea-9487-cf1d95616eb4.png)

Así como nos había pasado anteriormente cuando queríamos eliminarnos el problema de las funciones constantes dado que nuestro semi-prod interno $\int \nabla u \nabla v dx$  no las diferenciaba, por lo que no podemos usar Riesz para garantizarnos la unicidad, siempre nos va  quedar salvo una constante. Entonces hacemos como hicimos la otra vez de poner las funciones con promedio exactamente igual a 0 que denotaremos $L^2_0(\Bbb R^n)$. Lo bueno de esto es que vamos a poder usar una acotación para $L^2(\Bbb R^n)$ que nos va a ser de gran utilidad para reescribir nuestro problema como

![image](https://user-images.githubusercontent.com/31391855/90340724-a43eeb80-dfd0-11ea-86f8-9480f0d638bc.png)
y ahora sí poder usar Riesz para tener existencia y unicidad.

>   <u>Comentario:</u> Tuvimos que hacer este juego de cambiarnos las funciones para que tengan promedio 0 y todo esto, no por diversión sino para que nos quede un **producto interno** y así poder usar Riesz. 

## Extensión a operadores elípticos simétricos.

Imaginemos que ahora generalizamos el problema original tomando algo más complicado en vez de solo el laplaciano. Por ejemplo podríamos hacer de tomar una operador y mirar el problema más general del estilo,

![image](https://user-images.githubusercontent.com/31391855/90340731-b1f47100-dfd0-11ea-99b8-f34a8398a582.png)

### Caso simétrico(Riesz).

Si planteamos la formulación débil como veníamos haciendo para todos los casos anteriores y de vuelta recordemos que solo hay una herramienta y esta es el teorema de Riesz. Queremos que sea un producto interno tal que la norma que nos termina dando sea equivalente a la norma de $H^1_0$. Para esto vamos a necesitar que se cumplan algunas propiedades de la forma bilineal que obtenemos de nuestra $\cal L$ que llamaremos $B[u,v]$. Si escribimos de la manera más general tenemos que tiene la siguiente pinta,

![image](https://user-images.githubusercontent.com/31391855/90340750-ccc6e580-dfd0-11ea-924b-e54e9fc06a53.png)


y las condiciones que surgen para sus coeficientes son las siguientes

1.  $a_{ij}, b_{i}, c \in L^{\infty}(U)$ para que $B$ sea bilineal y continua.
2. $a_{ij} = a_{ji}$  y $b=0$ para que sea simétrico que es una de las cosillas que les pedimos a los productos internos.
3. si le pedimos que sea **uniformemente elíptico** es decir que exista una constante $\theta$ tal que haga valer la siguiente desigualdad,

![image](https://user-images.githubusercontent.com/31391855/90340759-dd775b80-dfd0-11ea-8094-c56957fa3a26.png)


Si tenemos que vale $c \ge 0$ o que vale $||c||_{\infty} < \theta \lambda_1$ entonces $B$ es un producto interno dado que $B[u,u]=0 \Leftrightarrow u=0$ y luego podemos ver que es equivalente a la norma de $H^1_0$.

Si se cumplen estas condiciones podemos usar Riesz y por lo tanto tenemos el siguiente jugoso resultado,

![image](https://user-images.githubusercontent.com/31391855/90340782-fc75ed80-dfd0-11ea-9604-b2e5c9b8a6d8.png)



### Caso no simétrico (Lax Milgram)

¿Qué pasa si no resulta ser simétrico?

 En tal caso no tenemos una forma bilineal que nos da un prod interno pero existe un resultado de análisis funcional que nos salva las papas. El teorema de **Lax Milgram**,
![image](https://user-images.githubusercontent.com/31391855/90340795-0861af80-dfd1-11ea-83a2-d0c886ed20c3.png)

que generaliza al teorema de Riesz pero con la hipótesis más débil en este caso de que sea coerciva.

#### Una manera de conseguir coercividad.

 Así podemos hacer como hicimos antes y en este caso tener que el operador $\cal L$ va a tener soluciones al problema sin tener que pedirle que su forma bilineal asociada sea simétrica! Esto lo traducimos a los términos de la forma de la siguiente manera,

![image](https://user-images.githubusercontent.com/31391855/90340810-13b4db00-dfd1-11ea-91b0-e7e35e5fc452.png)

#### Otra manera de conseguir coercividad.

Pensemos otras hipótesis que le podemos pedir para tener coercividad y así poder usar el teo de Lax-Milgram. Para esto necesitamos agregarle un término a nuestro operador $\cal L$. Esto es considerar el siguiente problema,

![image](https://user-images.githubusercontent.com/31391855/90340825-229b8d80-dfd1-11ea-9ac5-2907ec264717.png)

donde agregamos un parámetro extra $\gamma$ que nos va a ser muy útil después porque lo podemos elegir de manera que nos de coerciva. Básicamente hacemos cuentas de análisis usando algunas desigualdades como siempre y llegamos a la condicion,

![image](https://user-images.githubusercontent.com/31391855/90340829-2af3c880-dfd1-11ea-94ea-b919b274625c.png)

y en este caso nuestra $B_{\gamma}$ es coerciva y podemos aplicar Lax-Milgram para obtener la solución (única) débil del problema anterior.



## Propiedades del operador $\cal L$.

Consideremos su inversa,
$$\cal L ^ {-1} : f \to u$$
y vamos a ver que propiedades nos pasa $f$ a $u$ por medio de $\cal L^{-1}$.  

### Principio del máximo.

El primer resultado que vamos a observar es el siguiente. Si nuestro operador es unif elíptico, $c \ge 0$, simétrico y todo lo lindo que supusimos antes tenemos el siguiente resultado.

![image](https://user-images.githubusercontent.com/31391855/90340871-6a221980-dfd1-11ea-932e-d429d350e683.png)

que básicamente nos controla a nuestra función solución por medio de la $f$.

### Continuidad y compacidad de $\cal L ^{-1}$.

Supongamos ahora que verifica las propiedades del teo de Lax-Milgram. Es decir estamos pidiendo un poquito menos que antes para el pcpio del máximo. En este caso tenemos el hermoso resultado que nos dice lo siguiente,

![image](https://user-images.githubusercontent.com/31391855/90340874-74441800-dfd1-11ea-85cf-8f1b4d30beaf.png)

donde al ser lineal y continuo vale la cota que pusimos abajo. 



Una vez que obtuvimos esto podemos usar nuestro querido resultado R-K obtenido anteriormente para ver que $\cal{L}^{-1}$ es compacto. Esto es que dada una sucesión acotada $(f)_k$ tenemos una subsucesión de $\cal L^{-1}(f_k)$ que converge en $L^2(U)$ simplemente usando el resultado anteriormente mencionado.

### Adjunto de $\cal{L}$.

Así como hacíamos para álgebra lineal nos interesa resolver los casos del estilo $Ax=b$ y entender en términos de cuando no se pueda resolver cual es su núcleo (es decir que debería ser no trivial). Podemos recordar que $Ax=b$ tiene solución sii $bv=0 \ \ \forall v \in Nu(A^{*})$. 

Lo que vamos a hacer es llevar esta analogía a nuestro caso cuando $A=\cal L$ y $b = f$. Si consideramos el adjunto del operador $\cal L$ como
![image](https://user-images.githubusercontent.com/31391855/90340884-81610700-dfd1-11ea-83a7-6aa8f4a78877.png)

entonces obtenemos el siguiente resultado bastante similar en espírutu al resultado de álgebra lineal para la ecuación $\cal L u = f, \ \ u=0$,

![image](https://user-images.githubusercontent.com/31391855/90340890-8d4cc900-dfd1-11ea-911c-7d8f3793d3c6.png)


## Método de separación de variables.

Volvamos al comienzo de la materia. La pregunta es 

¿por qué? 

La respuesta es que queremos ver en el problema de la ecuación del calor en un abierto acotado $U \subset \Bbb R^n$ y $f \in L^2(U)$:

![image](https://user-images.githubusercontent.com/31391855/90340900-9f2e6c00-dfd1-11ea-8190-5531e25e795e.png)

Si la solución obtenida por este método de sep de variables es única. Anteriormente nos poníamos a jugar con las hipótesis de $f$ y demás para garantizar esto. Pero si sabemos que $u$ es solución débil en el sentido de estar en $C([0,T], L^2[0,T]) \cap L^2([0,T], H^1_0(U))$  y cumplir que resuelve debilmente la ecuación entonces tenemos existencia y unicidad, esto es que

![image](https://user-images.githubusercontent.com/31391855/90340912-ab1a2e00-dfd1-11ea-9668-f8d1bab9a492.png)

Y ahora vamos por más. Recordemos que la ecuación de calor a dif de la de ondas y la de transporte tenía el poder mágico de ser regularizante. Veamos que si $D=(0,T)\times U$ luego cualquier sol. de la ecuación del calor en el sentido de distribución es $C^{\infty}(D).$





---

---

## Ejemplos.

### Si queremos ver algo en sentido débil.

Recordemos que si queremos ver alguna igualdad en el sentido débil, que tiene que valer para todas las $\phi \in C^{\infty}_c(U)$. En particular si queremos romper algo podemos tomarnos las funciones de soporte compacto que nos convengan. Por ejemplo podemos tomarnos las que tienen un pico en un punto del interior de $U$ y en todos los otros puntos se van tendiendo a $0$.

### Pasitos para resolver problemas de autovalores.

1. Primero miramos que la ec no homogenea,
   $$   - \Delta u = f $$
   $$ u = 0 $$
   hay que usar Lax-Millgram y/o Riesz para conseguir las soluciones a la ecuación original y si no podés, sos voleta. Quizá no sale de una y hay que usar una desigualdad tipo Poincaré para poder estar en condiciones.

2.  Estudiamos que la aplicación $Tf \to u$ es cont lineal, compacta y simétrica. Hacemos todo con la formulación débil, usando funciones test adecuadas.

3. Por teo de espacios de Hilbert si cumple las condiciones anteriores nos queda que es diagonalizable tal como queríamos ver.

#### $H_0^2 \subset H^2 \cap H_0^1 $

Notemos que es una inclusión estricta. Porque estamos diciendo que hay convergencia en $H^2$ para sucesiones de funciones de soporte compacto. Esto nos dice que estas funciones son tales que sus gradientes están en $H^1_0$ por lo tanto por medio de la traza sabemos que vale la condición de Neumann en el borde. No necesariamente vale que el gradiente de una función esté en $H^1_0$ por este motivo decimos que la inclusión es estricta!

---

Para entender mejor estos temas podemos chequear el siguiente libro:

----->  $\fbox {"Sobolev Spaces", Adams-Fournier} $
