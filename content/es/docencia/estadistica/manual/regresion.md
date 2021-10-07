---
title: Regresión
summary: " " 
date: 
lastmod:
tags: [Correlación, Regresión, Regresión Lineal, Regresión No Lineal]
categories: [Estadística, Bioestadística]
type: book
weight: 20
---

Hasta ahora se ha visto como describir el comportamiento de una variable, pero en los fenómenos naturales normalmente aparecen más de una variable que suelen estar relacionadas. Por ejemplo, en un estudio sobre el peso de las personas, deberíamos incluir todas las variables con las que podría tener relación: altura, edad, sexo, dieta, tabaco,
ejercicio físico, etc.

Para comprender el fenómeno no basta con estudiar cada variable por separado y es preciso un estudio conjunto de todas las variables para ver cómo interactúan y qué relaciones se dan entre ellas. El objetivo de la estadística en este caso es dar medidas del grado y del tipo de relación entre dichas variables.

Generalmente, en un _estudio de dependencia_ se considera una **variable dependiente** $Y$ que se supone relacionada con otras variables $X_1,\ldots,X_n$ llamadas **variables independientes**.

El caso más simple es el de una sola variable independiente, y en tal caso se habla de _estudio de dependencia simple_. Para más de una
variable independiente se habla de _estudio de dependencia múltiple_.

En este capítulo se verán los estudios de dependencia simple que son más sencillos.

## Distribución de frecuencias conjunta

### Frecuencias conjuntas

Al estudiar la dependencia simple entre dos variables $X$ e $Y$, no se pueden estudiar sus distribuciones por separado, sino que hay que estudiar la distribución conjunta de la **variable bidimensional** $(X,Y)$, cuyos valores son los pares $(x_i,y_j)$ donde el primer elemento es un valor $X$ y el segundo uno de $Y$.

{{% alert def %}}
**Definición - Frecuencias muestrales conjuntas**. Dada una muestra de tamaño $n$ de una variable bidimensional $(X,Y)$, para cada valor de la variable $(x_i,y_j)$ observado en la muestra se define

- **Frecuencia absoluta** $n_{ij}$: Es el número de veces que el par $(x_i,y_j)$ aparece en la muestra.
- **Frecuencia relativa** $f_{ij}$: Es la proporción de veces que el par $(x_i,y_j)$ aparece en la muestra.
  
$$f_{ij}=\frac{n_{ij}}{n}$$
{{% /alert %}}

{{% alert warning %}}
Para las variables bidimensionales no tienen sentido las frecuencias acumuladas.
{{% /alert %}}

### Distribución de frecuencias bidimensional

Al conjunto de valores de la variable bidimensional y sus respectivas frecuencias muestrales se le denomina **distribución de frecuencias bidimensional**, y se representa mediante una **tabla de frecuencias bidimensional**.

$$\begin{array}{|c|ccccc|}
\hline
X\backslash Y & y_1 & \cdots & y_j & \cdots & y_q\newline
\hline
x_1 & n_{11} & \cdots & n_{1j} & \cdots & n_{1q}\newline
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots\newline
x_i & n_{i1} & \cdots & n_{ij} & \cdots & n_{iq}\newline
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots\newline
x_p & n_{p1} & \cdots & n_{pj} & \cdots & n_{pq}\newline
\hline
\end{array}$$

**Ejemplo (datos agrupados)**. La estatura (en cm) y el peso (en Kg) de una muestra de 30 estudiantes es:

<div style="text-align:center">
(179,85), (173,65), (181,71), (170,65), (158,51), (174,66),<br/>
(172,62), (166,60), (194,90), (185,75), (162,55), (187,78),<br/>
(198,109), (177,61), (178,70), (165,58), (154,50), (183,93),<br/>
(166,51), (171,65), (175,70), (182,60), (167,59), (169,62),<br/>
(172,70), (186,71), (172,54), (176,68),(168,67), (187,80).
</div>

La tabla de frecuencias bidimensional es

$$\begin{array}{|c||c|c|c|c|c|c|}
\hline
  X/Y & [50,60) & [60,70) & [70,80) & [80,90) & [90,100) & [100,110) \newline
  \hline\hline
  (150,160] & 2 & 0 & 0 & 0 & 0 & 0 \newline
  \hline
  (160,170] & 4 & 4 & 0 & 0 & 0 & 0 \newline
  \hline
  (170,180] & 1 & 6 & 3 & 1 & 0 & 0 \newline
  \hline
  (180,190] & 0 & 1 & 4 & 1 & 1 & 0 \newline
  \hline
  (190,200] & 0 & 0 & 0 & 0 & 1 & 1 \newline
  \hline
\end{array}$$

### Diagrama de dispersión

La distribución de frecuencias conjunta de una variable bidimensional puede representarse gráficamente mediante un **diagrama de dispersión**, donde los datos se representan como una colección de puntos en un plano cartesiano.

Habitualmente la variable independiente se representa en el eje $X$ y la variable dependiente en el eje $Y$. Por cada par de valores $(x_i,y_j)$ en la muestra se dibuja un punto en el plano con esas coordenadas.

<img src="../img/regresion/diagrama_dispersion.svg" alt="Diagrama de dispersión" width="300">

El resultado es un conjunto de puntos que se conoce como _nube de puntos_.

**Ejemplo**. El siguiente diagrama de dispersión representa la distribución conjunta de estaturas y pesos de la muestra anterior.

<img src="../img/regresion/diagrama_dispersion_estatura_peso.svg" alt="Diagrama de dispersión de estaturas y pesos" width="600">

{{% alert int %}}
El diagrama de dispersión da información visual sobre el tipo de relación entre las variables.

<img src="../img/regresion/diagrama_dispersion_tipos_relaciones.svg" alt="Diagramas de dispersión de diferentes tipos de relaciones" width="700">
{{% /alert %}}

### Distribuciones marginales

A cada una de las distribuciones de las variables que conforman la
variable bidimensional se les llama .

Las distribuciones marginales se pueden obtener a partir de la tabla de
frecuencias bidimensional, sumando las frecuencias por filas y columnas.

$$
\begin{array}{|c|ccccc|c|}
\hline
X\backslash Y & y_1 & \cdots & y_j & \cdots & y_q & \color{red}{n_x}\newline
\hline
x_1 & n_{11} & \cdots & n_{1j} & \cdots & n_{1q} & \color{red}{n_{x_1}}\newline
\vdots & \vdots & \vdots & \downarrow + & \vdots & \vdots & \color{red}{\vdots} \newline
x_i & n_{i1} & \stackrel{+}{\rightarrow} & n_{ij} & \stackrel{+}{\rightarrow} & n_{iq} & \color{red}{n_{x_i}}\newline
\vdots & \vdots & \vdots & \downarrow +  & \vdots & \vdots & \color{red}{\vdots}\newline
x_p & n_{p1} & \cdots & n_{pj} & \cdots & n_{pq} & \color{red}{n_{x_p}} \newline
\hline
\color{red}{n_y} & \color{red}{n_{y_1}} & \color{red}{\cdots} & \color{red}{n_{y_j}} & \color{red}{\cdots} & \color{red}{n_{y_q}} & n\newline
\hline
\end{array}
$$

**Ejemplo**. En el ejemplo anterior de las estaturas y los pesos, las distribuciones marginales son

$$
\begin{array}{|c||c|c|c|c|c|c|c|}
\hline
  X/Y & [50,60) & [60,70) & [70,80) & [80,90) & [90,100) & [100,110) & \color{red}{n_x}\newline
  \hline\hline
  (150,160] & 2 & 0 & 0 & 0 & 0 & 0 & \color{red}{2}\newline
  \hline
  (160,170] & 4 & 4 & 0 & 0 & 0 & 0 & \color{red}{8}\newline
  \hline
  (170,180] & 1 & 6 & 3 & 1 & 0 & 0 & \color{red}{11} \newline
  \hline
  (180,190] & 0 & 1 & 4 & 1 & 1 & 0 & \color{red}{7} \newline
  \hline
  (190,200] & 0 & 0 & 0 & 0 & 1 & 1 & \color{red}{2}\newline
  \hline
  \color{red}{n_y} & \color{red}{7} & \color{red}{11} & \color{red}{7} & \color{red}{2} & \color{red}{2} & \color{red}{1} & 30\newline
  \hline
\end{array}
$$

y los estadísticos correspondientes son

$$
\begin{array}{lllll}
\bar x = 174.67 \mbox{ cm} & \quad & s^2_x = 102.06 \mbox{ cm}^2 & \quad & s_x = 10.1 \mbox{ cm}\newline
\bar y = 69.67 \mbox{ Kg} & & s^2_y = 164.42 \mbox{ Kg}^2 & & s_y = 12.82 \mbox{ Kg}
\end{array}
$$

## Covarianza

Para analizar la relación entre dos variables cuantitativas es importante hacer un estudio conjunto de las desviaciones respecto de la media de cada variable.

<img src="../img/regresion/desviaciones_media.svg" alt="Desviaciones de las medias en un diagrama de dispersión" width="600">

Si dividimos la nube de puntos del diagrama de dispersión en 4 cuadrantes centrados en el punto de medias $(\bar x, \bar y)$, el signo de las desviaciones será:

   |**Cuadrante**|$(x_i-\bar x)$|$(y_j-\bar y)$|$(x_i-\bar x)(y_j-\bar y)$|
   |:-----------:|:------------:|:------------:|:------------------------:|
   |      1      |      $+$     |      $+$     |           $+$            |
   |      2      |      $-$     |      $+$     |           $-$            |
   |      3      |      $-$     |      $-$     |           $+$            |
   |      4      |      $+$     |      $-$     |           $-$            |

<img src="../img/regresion/cuadrantes_diagrama_dispersion.svg" alt="Cuadrantes de un diagrama de dispersión" width="400">

Si la relación entre las variables es _lineal y creciente_, entonces la mayor parte de los puntos estarán en los cuadrantes 1 y 3 y la suma de los productos de desviaciones será positiva.

$$\sum(x_i-\bar x)(y_j-\bar y) > 0$$

<img src="../img/regresion/diagrama_dispersion_lineal_creciente.svg" alt="Diagrama de dispersión de una relación lineal creciente" width="500">

Si la relación entre las variables es _lineal y decreciente_, entonces la mayor parte de los puntos estarán en los cuadrantes 2 y 4 y la suma de los productos de desviaciones será negativa.

$$\sum(x_i-\bar x)(y_j-\bar y) = -$$

<img src="../img/regresion/diagrama_dispersion_lineal_decreciente.svg" alt="Diagrama de dispersión de una relación lineal decreciente" width="500">

Usando el producto de las desviaciones respecto de las medias surge el
siguiente estadístico.

{{% alert def %}}
**Definición - Covarianza muestral**. La _covarianza muestral_ de una variable aleatoria bidimensional $(X,Y)$ se define como el promedio de los productos de las respectivas desviaciones respecto de las medias de $X$ e $Y$.

$$s_{xy}=\frac{\sum (x_i-\bar x)(y_j-\bar y)n_{ij}}{n}$$
{{% /alert %}}

También puede calcularse de manera más sencilla mediante la fórmula

$$s_{xy}=\frac{\sum x_iy_jn_{ij}}{n}-\bar x\bar y.$$

{{% alert int %}}
La covarianza sirve para estudiar la relación lineal entre dos variables:

- Si $s_{xy}>0$ existe una relación lineal creciente.
- Si $s_{xy}<0$ existe una relación lineal decreciente.
- Si $s_{xy}=0$ no existe relación lineal.
{{% /alert %}}

**Ejemplo**. Utilizando la tabla de frecuencias bidimensional de la muestra de estaturas y pesos

$$
\begin{array}{|c||c|c|c|c|c|c|c|}
\hline
  X/Y & [50,60) & [60,70) & [70,80) & [80,90) & [90,100) & [100,110) & n_x\newline
  \hline\hline
  (150,160] & 2 & 0 & 0 & 0 & 0 & 0 & 2\newline
  \hline
  (160,170] & 4 & 4 & 0 & 0 & 0 & 0 & 8\newline
  \hline
  (170,180] & 1 & 6 & 3 & 1 & 0 & 0 & 11 \newline
  \hline
  (180,190] & 0 & 1 & 4 & 1 & 1 & 0 & 7 \newline
  \hline
  (190,200] & 0 & 0 & 0 & 0 & 1 & 1 & 2\newline
  \hline
  n_y & 7 & 11 & 7 & 2 & 2 & 1 & 30\newline
  \hline
\end{array}
$$

$$\bar x = 174.67 \mbox{ cm} \qquad \bar y = 69.67 \mbox{ Kg}$$

la covarianza vale

$$
\begin{aligned}
s_{xy} &=\frac{\sum x_iy_jn_{ij}}{n}-\bar x\bar y =  \frac{155\cdot 55\cdot 2 + 165\cdot 55\cdot 4 + \cdots + 195\cdot 105\cdot 1}{30}-174.67\cdot 69.67 =\newline
& = \frac{368200}{30}-12169.26 = 104.07 \mbox{ cm$\cdot$ Kg}.
\end{aligned}
$$

Esto indica que existe una relación lineal creciente entre la estatura y el peso.

## Regresión

En muchos casos el objetivo de un estudio no es solo detectar una relación entre dos variables, sino explicarla mediante alguna función matemática $$y=f(x)$$ que permita predecir la variable dependiente para cada valor de la independiente.

La **regresión** es la parte de la Estadística encargada de construir esta función, que se conoce como **función de regresión** o **modelo de regresión**.

### Modelos de regresión simple

Dependiendo de la forma de función de regresión, existen muchos tipos de
regresión simple. Los más habituales son los que aparecen en la
siguiente tabla:

| **Modelo**  |     **Ecuación**      |
|:------------|:---------------------:|
| Lineal      |       $y=a+bx$        |
| Cuadrático  |     $y=a+bx+cx^2$     |
| Cúbico      |  $y=a+bx+cx^2+dx^3$   |
| Potencial   |    $y=a\cdot x^b$     |
| Exponencial |     $y=e^{a+bx}$      |
| Logarítmico |     $y=a+b\log x$     |
| Inverso     |   $y=a+\frac{b}{x}$   |
| Sigmoidal   | $y=e^{a+\frac{b}{x}}$ |

La elección de un tipo u otro depende de la forma que tenga la nube de puntos del diagrama de dispersión.

### Residuos o errores predictivos

Una vez elegida la familia de curvas que mejor se adapta a la nube de
puntos, se determina, dentro de dicha familia, la curva que mejor se
ajusta a la distribución, es decir, la función que mejor predice la variable dependiente.

El objetivo es encontrar la función de regresión que haga mínimas las
distancias entre los valores de la variable dependiente observados en la
muestra, y los predichos por la función de regresión. Estas distancias
se conocen como _residuos_ o _errores predictivos_.

{{% alert def %}}
**Definición - Residuos o errores predictivos**. Dado el modelo de regresión $y=f(x)$ para una variable bidimensional $(X,Y)$, el _residuo_ o _error predictivo_ de un valor $(x_i,y_j)$ observado en la muestra, es la diferencia entre el valor observado de la variable dependiente $y_j$ y el predicho por la función de regresión para $x_i$,

$$e_{ij} = y_j-f(x_i).$$
{{% /alert %}}

<img src="../img/regresion/residuos_y.svg" alt="Residuos de un modelo de regresión" width="600">

### Ajuste de mínimos cuadrados

Una forma posible de obtener la función de regresión es mediante el método de _mínimos cuadrados_ que consiste en calcular la función que haga mínima la suma de los cuadrados de los residuos

$$\sum e_{ij}^2.$$

En el caso de un modelo de regresión lineal $f(x) = a + bx$, como la recta depende de dos parámetros (el término independiente $a$ y la pendiente $b$), la suma también dependerá de estos parámetros

$$\theta(a,b) = \sum e_{ij}^2 =\sum (y_j - f(x_i))^2 =\sum (y_j-a-bx_i)^2.$$

Así pues, todo se reduce a buscar los valores $a$ y $b$ que hacen mínima esta suma.

Considerando la suma de los cuadrados de los residuos como una función de dos variables $\theta(a,b)$, se pueden calcular los valores de los parámetros del modelo que hacen mínima esta suma derivando e igualando a 0 las derivadas con respecto a $a$ y $b$.

$$
\begin{aligned}
\frac{\partial \theta(a,b)}{\partial a} &=  \frac{\partial \sum (y_j-a-bx_i)^2 }{\partial a} =0\newline
\frac{\partial \theta(a,b)}{\partial b} &=  \frac{\partial \sum (y_j-a-bx_i)^2 }{\partial b} =0
\end{aligned}
$$

Tras resolver el sistema se obtienen los valores

$$a= \bar y - \frac{s_{xy}}{s_x^2}\bar x \qquad b=\frac{s_{xy}}{s_x^2}$$

Estos valores hacen mínimos los residuos en $Y$ y por tanto dan la recta
de regresión óptima.

## Recta de regresión

{{% alert def %}}
**Definición - Recta de regresión**. Dada una variable bidimensional $(X,Y)$, la _recta de regresión_ de $Y$ sobre $X$ es

$$y = \bar y +\frac{s_{xy}}{s_x^2}(x-\bar x).$$
{{% /alert %}}

{{% alert int %}}
La recta de regresión de $Y$ sobre $X$ es la recta que hace mínimos los errores predictivos en $Y$, y por tanto es la recta que hará mejores predicciones de $Y$ para cualquier valor de $X$.
{{% /alert %}}

**Ejemplo**. Utilizando la muestra anterior de estaturas ($X$) y pesos ($Y$) con los siguientes estadísticos

$$
\begin{array}{lllll}
\bar x = 174.67 \mbox{ cm} & \quad & s^2_x = 102.06 \mbox{ cm}^2 & \quad & s_x = 10.1 \mbox{ cm}\newline
\bar y = 69.67 \mbox{ Kg} & & s^2_y = 164.42 \mbox{ Kg}^2 & & s_y = 12.82 \mbox{ Kg}\newline
& & s_{xy} = 104.07 \mbox{ cm$\cdot$ Kg} & &
\end{array}
$$

la recta de regresión del peso sobre la estatura es

$$y = \bar y +\frac{s_{xy}}{s_x^2}(x-\bar x) = 69.67+\frac{104.07}{102.06}(x-174.67) =  -108.49 + 1.02 x.$$

De igual modo, si tomamos la estatura como variable dependiente, la
recta de regresión de la estatura sobre el peso es

$$x = \bar x +\frac{s_{xy}}{s_y^2}(y-\bar y) = 174.67+\frac{104.07}{164.42}(y-69.67) = +130.78 + 0.63 y.$$

{{% alert warning %}}
¡Obsérvese que ambas rectas de regresión son diferentes!
{{% /alert %}}

<img src="../img/regresion/rectas_regresion.svg" alt="Rectas de regresión de estaturas y pesos" width="600">

### Posición relativa de las rectas de regresión

Habitualmente, las rectas de regresión $Y$ sobre $X$ y de $X$ sobre $Y$ no coinciden, pero siempre se cortan en el punto de medias $(\bar x,\bar y)$.

Si entre las variables la relación lineal es perfecta, entonces ambas rectas coinciden ya que esa recta hace tanto los residuos en $X$ como los residuos en $Y$ nulos.

<img src="../img/regresion/regresion_lineal_perfecta.svg" alt="Recta de regresión de una relación lineal perfecta" width="500">

Si no hay relación lineal, entonces las ecuaciones de las rectas son constantes e iguales a las respectivas medias,

$$y = \bar y,\quad x = \bar x,$$

y se cortan perpendicularmente.

<img src="../img/regresion/rectas_independencia_lineal.svg" alt="Rectas de regresión de dos variables linealmente independientes" width="500">

### Coeficiente de regresión

El parámetro más importante de una recta de regresión es su pendiente.

{{% alert def %}}
**Definición - Coeficiente de regresión** $b_{yx}$. Dada una variable bidimensional $(X,Y)$, el _coeficiente de regresión_ de la recta de regresión de $Y$ sobre $X$ es su pendiente,

$$b_{yx} = \frac{s_{xy}}{s_x^2}$$
{{% /alert %}}

{{% alert warning %}}
El coeficiente de regresión siempre tiene el mismo signo que la covarianza.
{{% /alert %}}

{{% alert int %}}
Refleja el crecimiento de la variable dependiente en relación a la independiente según la recta de regresión. En concreto da el número de unidades que aumenta o disminuye la variable dependiente por cada unidad que aumenta la variable independiente.
{{% /alert %}}

**Ejemplo**. En el ejemplo de las estaturas y los pesos, la recta de regresión del
peso sobre la estatura era

$$y=-108.49 +1.02 x,$$

de manera que el coeficiente de regresión del peso sobre la estatura es

$$b_{yx}= 1.02 \mbox{Kg/cm.}$$

Esto significa que, según la recta de regresión del peso sobre la estatura, por cada cm más de estatura, la persona pesará $1.02$ Kg más.

### Predicciones con las rectas de regresión

Las rectas de regresión, y en general cualquier modelo de regresión, suele utilizarse con fines predictivos.

**Ejemplo**. En la muestra de las estaturas y los pesos, si se quiere predecir
el peso de una persona que mide 180 cm, se debe utilizar la recta de regresión del peso sobre la estatura,

$$y = 1.02 \cdot 180 -108.49 = 75.11 \mbox{ Kg}.$$

Y si se quiere predecir la estatura de una persona que pesa 79 Kg, se debe utilizar la recta de regresión de la estatura sobre el peso,

$$x = 0.63\cdot 79+ 130.78 = 180.55 \mbox{ cm}.$$

_Ahora bien, ¿qué fiabilidad tienen estas predicciones?_

## Correlación

Una vez construido un modelo de regresión, para saber si se trata de un buen modelo predictivo, se tiene que analizar el grado de dependencia entre las variables según el tipo de dependencia planteada en el modelo.
De ello se encarga la parte de la estadística conocida como **correlación**.

La correlación se basa en el estudio de los residuos: cuanto menores sean éstos, más se ajustará la curva de regresión a los puntos, y más intensa será la correlación.

### Varianza residual muestral

Una medida de la bondad del ajuste del modelo de regresión es la
_varianza residual_.

{{% alert def %}}
**Definición - Varianza residual muestral** $s_{ry}^2$. Dado un modelo de regresión simple $y=f(x)$ de una variable bidimensional $(X,Y)$, su _varianza residual muestral_ es el promedio de los cuadrados de los residuos para los valores de la muestra,

$$s_{ry}^2 = \frac{\sum e_{ij}^2n_{ij}}{n} = \frac{\sum (y_j - f(x_i))^2n_{ij}}{n}.$$
{{% /alert %}}

{{% alert int %}}
Cuanto más alejados estén los puntos de la curva de regresión, mayor será la varianza residual y menor la dependencia.

Cuando la relación lineal es perfecta los residuos se anulan y la varianza residual vale cero. Por contra, cuando no existe relación, los residuos coinciden con las desviaciones de la media, y la varianza residual es igual a la varianza de la variable dependiente.

$$0\leq s_{ry}^2\leq s_y^2$$
{{% /alert %}}

### Descomposición de la variabilidad total: Variabilidad explicada y no explicada

<img src="../img/regresion/variation_decomposition.gif" alt="Descomposición de la variabilidad de un modelo de regresión" width="600">

### Coeficiente de determinación

A partir de la varianza residual se puede definir otro estadístico más sencillo de interpretar.

{{% alert def %}}
**Definición - Coeficiente de determinación muestral $r^2$**. Dado un modelo de regresión simple $y=f(x)$ de una variable bidimensional $(X,Y)$, su _coeficiente de determinación muestral_ es

$$r^2 = 1- \frac{s_{ry}^2}{s_y^2}$$
{{% /alert %}}

{{% alert warning %}}
Como la varianza residual puede tomar valores entre 0 y $s_y^2$, se tiene que

$$0\leq r^2\leq 1$$
{{% /alert %}}

{{% alert int %}}
Cuanto mayor sea $r^2$, mejor explicará el modelo de regresión la relación entre las variables, en particular:

- Si $r^2 =0$ entonces no existe relación del tipo planteado por el modelo.
- Si $r^2=1$ entonces la relación que plantea el modelo es perfecta.
{{% /alert %}}

{{% alert warning %}}
En el caso de las rectas de regresión, el coeficiente de determinación puede calcularse con esta fórmula

$$ r^2 =  \frac{s_{xy}^2}{s_x^2s_y^2}.$$
{{% /alert %}}

{{< spoiler text="Demostración" >}}
Cuando el modelo ajustado es la recta de regresión la varianza residual vale

$$
\begin{aligned}
s_{ry}^2 & = \sum e_{ij}^2f_{ij} = \sum (y_j - f(x_i))^2f_{ij} = \sum \left(y_j - \bar y -\frac{s_{xy}}{s_x^2}(x_i-\bar x) \right)^2f_{ij}=\newline
& = \sum \left((y_j - \bar y)^2 +\frac{s_{xy}^2}{s_x^4}(x_i-\bar x)^2 - 2\frac{s_{xy}}{s_x^2}(x_i-\bar x)(y_j -\bar y)\right)f_{ij} =\newline
& = \sum (y_j - \bar y)^2f_{ij} +\frac{s_{xy}^2}{s_x^4}\sum (x_i-\bar x)^2f_{ij}- 2\frac{s_{xy}}{s_x^2}\sum (x_i-\bar x)(y_j -\bar y)f_{ij}=\newline
& = s_y^2 + \frac{s_{xy}^2}{s_x^4}s_x^2 - 2 \frac{s_{xy}}{s_x^2}s_{xy} = s_y^2 - \frac{s_{xy}^2}{s_x^2}.
\end{aligned}
$$

y, por tanto, el coeficiente de determinación lineal vale

$$
\begin{aligned}
r^2 &= 1- \frac{s_{ry}^2}{s_y^2} = 1- \frac{s_y^2 - \frac{s_{xy}^2}{s_x^2}}{s_y^2} = 1 - 1 + \frac{s_{xy}^2}{s_x^2s_y^2} = \frac{s_{xy}^2}{s_x^2s_y^2}.
\end{aligned}
$$
{{< /spoiler >}}

**Ejemplo**. En el ejemplo de las estaturas y pesos se tenía

$$
\begin{array}{lll}
\bar x = 174.67 \mbox{ cm} & \quad & s^2_x = 102.06 \mbox{ cm}^2\newline
\bar y = 69.67 \mbox{ Kg} & & s^2_y = 164.42 \mbox{ Kg}^2\newline
s_{xy} = 104.07 \mbox{ cm$\cdot$ Kg}
\end{array}
$$

De modo que el coeficiente de determinación lineal vale

$$r^2 = \frac{s_{xy}^2}{s_x^2s_y^2} = \frac{(104.07 \mbox{ cm\cdot Kg})^2}{102.06 \mbox{ cm}^2 \cdot 164.42 \mbox{ Kg}^2} = 0.65.$$

Esto indica que la recta de regresión del peso sobre la estatura explica el 65% de la variabilidad del peso, y de igual modo, la recta de regresión de la estatura sobre el peso explica el 65% de la variabilidad de la estatura.

### Coeficiente de correlación lineal

{{% alert def %}}
**Definición - Coeficiente de correlación lineal muestral**. Dada una variable bidimensional $(X,Y)$, el _coeficiente de correlación lineal muestral_ es la raíz cuadrada de su coeficiente de determinación lineal, con signo el de la covarianza

$$r = \sqrt{r^2} = \dfrac{s_{xy}}{s_xs_y}.$$
{{% /alert %}}

{{% alert warning %}}
Como $r^2$ toma valores entre 0 y 1, $r$ tomará valores entre -1 y 1,

$$-1\leq r\leq 1$$
{{% /alert %}}

{{% alert int %}}
El coeficiente de correlación lineal no sólo mide mide el grado de dependencia
lineal sino también su dirección (creciente o decreciente):

- Si $r =0$ entonces no existe relación lineal.
- Si $r=1$ entonces existe una relación lineal creciente perfecta.
- Si $r=-1$ entonces existe una relación lineal decreciente perfecta.
{{% /alert %}}

**Ejemplo**. En el ejemplo de las estaturas y los pesos se tenía

$$
\begin{array}{lll}
\bar x = 174.67 \mbox{ cm} & \quad & s^2_x = 102.06 \mbox{ cm}^2\newline
\bar y = 69.67 \mbox{ Kg} & & s^2_y = 164.42 \mbox{ Kg}^2\newline
s_{xy} = 104.07 \mbox{ cm$\cdot$ Kg}
\end{array}
$$

De manera que el coeficiente de correlación lineal es

$$r = \frac{s_{xy}}{s_xs_y} = \frac{104.07 \mbox{ cm\cdot Kg}}{10.1 \mbox{ cm} \cdot 12.82 \mbox{ Kg}} = +0.8.$$

Esto indica que la relación lineal entre el peso y la estatura es fuerte, y además creciente.

### Distintos grados de correlación

Los siguientes diagramas de dispersión muestran modelos de regresión lineales con diferentes grados de correlación.

<img src="../img/regresion/grados_correlacion.svg" alt="Modelos de regresión lineales con diferentes grados de correlación" width="700">

### Fiabilidad de las predicciones de un modelo de regresión

Aunque el coeficiente de determinación o el de correlación determinan la bondad de ajuste de un modelo de regresión, existen otros factores que influyen en la fiabilidad de las predicciones de un modelo de regresión:

- El coeficiente de determinación: Cuanto mayor sea, menores serán los errores predictivos y mayor la fiabilidad de las predicciones.
- La variabilidad de la población: Cuanto más variable es una población, más difícil es predecir y por tanto menos fiables serán las predicciones.
- El tamaño muestral: Cuanto mayor sea, más información tendremos y, en consecuencia, más fiables serán las predicciones.

{{% alert warning %}}
Además, hay que tener en cuenta que un modelo de regresión es válido únicamente para el rango de valores observados en la muestra. Fuera de ese rango no hay información del tipo de relación entre las variables, por lo que no deben hacerse predicciones para valores lejos de los observados en la muestra.
{{% /alert %}}

## Regresión no lineal

El ajuste de un modelo de regresión no lineal es similar al del modelo lineal y también puede realizarse mediante la técnica de mínimos cuadrados.

No obstante, en determinados casos un ajuste no lineal puede convertirse en un ajuste lineal mediante una sencilla transformación de alguna de las variables del modelo.

### Transformación de modelos de regresión no lineales

- **Logarítmico**: Un modelo logarítmico $y = a+b \log x$ se convierte en un modelo lineal haciendo el cambio $t=\log x$:

    $$y=a+b\log x = a+bt.$$

- **Exponencial**: Un modelo exponencial $y = ae^{bx}$ se convierte en un modelo
    lineal haciendo el cambio $z = \log y$:

    $$z = \log y = \log(ae^{bx}) =  \log a + \log e^{bx} = a^\prime +bx.$$

- **Potencial**: Un modelo potencial $y = ax^b$ se convierte en un modelo lineal
    haciendo los cambios $t=\log x$ y $z=\log y$:

    $$z = \log y = \log(ax^b) = \log a + b \log x = a^\prime+bt.$$

- **Inverso**: Un modelo inverso $y = a+b/x$ se convierte en un modelo lineal
    haciendo el cambio $t=1/x$:

    $$y = a + b(1/x) = a+bt.$$

- **Sigmoidal**: Un modelo curva S $y = e^{a+b/x}$ se convierte en un modelo lineal haciendo los cambios $t=1/x$ y $z=\log y$:

    $$z = \log y = \log (e^{a+b/x}) = a+b(1/x) = a+bt.$$

### Relación exponencial

**Ejemplo** El número de bacterias de un cultivo evoluciona con el tiempo según la
siguiente tabla:

$$\begin{array}{c|c}
\mbox{Horas} & \mbox{Bacterias}\newline
\hline
0 &  25 \newline
1 & 28 \newline
2 &  47\newline
3 & 65 \newline
4 & 86\newline
5 & 121\newline
6 & 190\newline
7 & 290\newline
8 & 362
\end{array}
$$

El diagrama de dispersión asociado es

<img src="../img/regresion/evolucion_bacterias.svg" alt="Diagrama de dispersión de la evolución de bacterias" width="500">

Si realizamos un ajuste lineal, obtenemos la siguiente recta de regresión

$$\mbox{Bacterias} = -30.18+41,27\,\mbox{Horas, with } r^2=0.85.$$

<img src="../img/regresion/regresion_lineal_bacterias.svg" alt="Regresión lineal de la evolución de un cultivo de bacterias" width="500">

_¿Es un buen modelo?_

Aunque el modelo lineal no es malo, de acuerdo al diagrama de dispersión es más lógico construir un modelo exponencial o cuadrático.

Para construir el modelo exponencial $y = ae^{bx}$ hay que realizar la
transformación $z=\log y$, es decir, aplicar el logaritmo a la variable dependiente.

$$\begin{array}{c|c|c}
\mbox{Horas} & \mbox{Bacterias} & \mbox{$\log$(Bacterias)}\newline
\hline
0 &  25 & 3.22\newline
1 & 28 & 3.33\newline
2 &  47 & 3.85\newline
3 & 65  & 4.17\newline
4 & 86 & 4.45\newline
5 & 121 & 4.80\newline
6 & 190 & 5.25\newline
7 & 290 & 5.67\newline
8 & 362 & 5.89
\end{array}
$$

<img src="../img/regresion/evolucion_log_bacterias.svg" alt="Diagrama de dispersión de la evolución del logarítmo de las bacterias de un cultivo" width="500">

Ahora sólo queda calcular la recta de regresión del logaritmo de Bacterias sobre Horas

$$\mbox{Log Bacterias} = 3.107 + 0.352\, \mbox{Horas}.$$

Y, deshaciendo el cambio de variable, se obtiene el modelo exponencial

$$\mbox{Bacterias} = e^{3.107+0.352\,\textrm{Horas}}, \mbox{ con } r^2=0.99.$$

<img src="../img/regresion/regresion_exponencial_bacterias.svg" alt="Regresión exponencial de la evolución de las bacterias de un cultivo" width="500">

Como se puede apreciar, el modelo exponencial se ajusta mucho mejor que el modelo lineal.

## Riesgos de la regresión

### La falta de ajuste no significa independencia

Es importante señalar que cada modelo de regresión tiene su propio coeficiente de determinación.

{{% alert warning %}}
Así, un coeficiente de determinación cercano a cero significa que no existe relación entre las variables del tipo planteado por el modelo, pero _eso no quiere decir que las variables sean independientes_, ya que puede existir relación de otro tipo.
{{% /alert %}}

<img src="../img/regresion/regresion_lineal_relacion_cuadratica.svg" alt="Modelo de regresión lineal en una relación cuadrática" width="500">
<img src="../img/regresion/regresion_cuadratica.svg" alt="Modelo de regresión cuadrático en una relación cuadrática" width="500">

### Datos atípicos en regresión

Los _datos atípicos_ en un estudio de regresión son los puntos que claramente no siguen la tendencia del resto de los puntos en el diagrama de dispersión, incluso si los valores del par no se pueden considerar atípicos para cada variable por separado.

<img src="../img/regresion/diagrama_dispersion_con_datos_atipicos.svg" alt="Diagrama de dispersión con un dato atípico" width="500">

{{% alert warning %}}
Los datos atípicos en regresión suelen provocar cambios drásticos en el ajuste de los modelos de regresión, y por tanto, habrá que tener mucho cuidado con ellos.
{{% /alert %}}

<div class="center">
<img src="../img/regresion/regresion_lineal_con_datos_atipicos.svg" alt="Modelo de regresión lineal con datos atípicos" width="500"> <img src="../img/regresion/regresion_lineal_sin_datos_atipicos.svg" alt="Modelo de regresión lineal sin datos atípicos" width="500">
</div>

### La paradoja de Simpson

A veces, una tendencia desaparece o incluso se revierte cuando se divide la muestra en grupos de acuerdo a una variable cualitativa que está relacionada con la variable dependiente.
Esto se conoce como la _paradoja de Simpson_.

**Ejemplo**. El siguiente diagrama de dispersión muestra una relación inversa entre entre las horas de estudio preparando un examen y la nota del examen.

<div class="center">
<img src="../img/regresion/paradoja_simpson_1.svg" alt="Paradoja de Simpson. Relación inversa entre las horas de estudio para un examen y la nota obtenida." width="500">
</div>

Pero si se divide la muestra en dos grupos (buenos y malos estudiantes) se obtienen diferentes tendencias y ahora la relación es directa, lo que tiene más lógica.

<div class="center">
<img src="../img/regresion/paradoja_simpson_2.svg" alt="Paradoja de Simpson. Relación directa entre las horas de estudio para un examen y la nota obtenida." width="500">
</div>