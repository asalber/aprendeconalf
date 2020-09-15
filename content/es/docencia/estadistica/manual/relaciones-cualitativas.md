---
title: Relaciones entre variables cualitativas
summary: " " 
date: 
lastmod:
tags: [Correlación, Asociación]
categories: [Estadística, Bioestadística]
type: book
weight: 25
---
Los modelos de regresión vistos sólo pueden aplicarse cuando las variables estudiadas son cuantitativas.

Cuando se desea estudiar la relación entre atributos, tanto ordinales como nominales, es necesario recurrir a otro tipo de medidas de relación o de asociación. En este capítulo veremos tres de ellas:

- Coeficiente de correlación de Spearman.
- Coeficiente chi-cuadrado.
- Coeficiente de contingencia.

## Relación entre atributos ordinales

### Coeficiente de correlación de Spearman

Cuando se tengan atributos ordinales es posible ordenar sus categorías y asignarles valores ordinales, de manera que se puede calcular el coeficiente de correlación lineal entre estos valores ordinales.

Esta medida de relación entre el orden que ocupan las categorías de dos atributos ordinales se conoce como _coeficiente de correlación de Spearman_.

{{% alert def %}}
**Definición - Coeficiente de correlación de Spearman**. Dada una muestra de $n$ individuos en los que se han medido dos atributos ordinales $X$ e $Y$, el coeficiente de correlación de Spearman se define como

$$r_s = 1-\frac{6\sum d_i^2}{n(n^2-1)}$$

donde $d_i$ es la diferencia entre el valor ordinal de $X$ y el valor ordinal de $Y$ del individuo $i$.
{{% /alert %}}

{{% alert warning %}}
Como el coeficiente de correlación de Spearman es en el fondo el coeficiente de correlación lineal aplicado a los órdenes, se tiene que

$$-1\leq r_s\leq 1,$$
{{% /alert %}}

{{% alert int %}}
- Si $r_s=0$ entonces no existe relación entre los atributos ordinales.
- Si $r_s=1$ entonces los órdenes de los atributos coinciden y existe una relación directa perfecta.
- Si $r_s=-1$ entonces los órdenes de los atributos están invertidos y existe una relación inversa perfecta.

En general, cuanto más cerca de $1$ o $-1$ esté $r_s$, mayor será la relación entre los atributos, y cuanto más cerca de $0$, menor será la relación.
{{% /alert %}}

**Ejemplo**. Una muestra de 5 alumnos realizaron dos tareas diferentes $X$ e $Y$, y se ordenaron de acuerdo a la destreza que manifestaron en cada tarea:

$$
\begin{array}{lrrrr}
\hline
\text{Alumnos} & X & Y & d_i & d_i^2\newline
\hline
\text{Alumno 1} & 2 & 3 & -1 & 1\newline
\text{Alumno 2} & 5 & 4 & 1 & 1 \newline
\text{Alumno 3} & 1 & 2 & -1 & 1\newline
\text{Alumno 4} & 3 & 1 & 2 & 4\newline
\text{Alumno 5} & 4 & 5 & -1 & 1\newline
\hline
\sum &  &  & 0 & 8 \newline
\hline
\end{array}
$$

El coeficiente de correlación de Spearman para esta muestra es

$$r_s = 1-\frac{6\sum d_i^2}{n(n^2-1)} = 1- \frac{6\cdot 8}{5(5^2-1)} = 0.6.$$

Esto indica que existe bastante relación directa entre las destrezas manifestadas en ambas tareas.

**Ejemplo con empates**.

Cuando hay empates en el orden de las categorías se atribuye a cada valor empatado la media aritmética de los valores ordinales que hubieran ocupado esos individuos en caso de no haber estado empatados.

Si en el ejemplo anterior los alumnos 4 y 5 se hubiesen comportado igual en la primera tarea y los alumnos 3 y 4 se hubiesen comportado igual en la segunda tarea, entonces se tendría

$$
\begin{array}{lrrrr}
\hline
\text{Alumnos} & X & Y & d_i & d_i^2\newline
\hline
\text{Alumno 1} & 2 & 3 & -1 & 1\newline
\text{Alumno 2} & 5 & 4 & 1 & 1 \newline
\text{Alumno 3} & 1 & 1.5 & -0.5 & 0.25\newline
\text{Alumno 4} & 3.5 & 1.5 & 2 & 4\newline
\text{Alumno 5} & 3.5 & 5 & -1.5 & 2.25\newline
\hline
\sum &  &  & 0 & 8.5 \newline
\hline
\end{array}
$$

El coeficiente de correlación de Spearman para esta muestra es

$$r_s = 1-\frac{6\sum d_i^2}{n(n^2-1)} = 1- \frac{6\cdot 8.5}{5(5^2-1)} = 0.58.$$

## Relación entre atributos nominales

Cuando se quiere estudiar la relación entre atributos nominales no tiene sentido calcular el coeficiente de correlación de Spearman ya que las categorías no pueden ordenarse.

Para estudiar la relación entre atributos nominales se utilizan medidas basadas en las frecuencias de la tabla de frecuencias bidimensional, que para atributos se suele llamar _tabla de contingencia_.

**Ejemplo**. En un estudio para ver si existe relación entre el sexo y el hábito de fumar se ha tomado una muestra de 100 personas. La tabla de contingencia resultante es

$$
\begin{array}{|l|rr|r|}
\hline
\text{Sexo}\backslash\text{Fuma} & \text{Si} & \text{No} & n_i\newline
\hline
\text{Mujer} & 12 & 28 & 40 \newline
\text{Hombre} & 26 & 34 & 60 \newline
\hline
n_j & 38 & 62 & 100\newline
\hline
\end{array}
$$

Si el hábito de fumar fuese independiente del sexo, la proporción de fumadores en mujeres y hombres sería la misma.

### Frecuencias teóricas o esperadas

En general, dada una tabla de contingencia para dos atributos $X$ e $Y$,

$$
\begin{array}{|c|ccccc|c|}
\hline
X\backslash Y & y_1 & \cdots & y_j & \cdots & y_q & n_x\newline
\hline
x_1 & n_{11} & \cdots & n_{1j} & \cdots & n_{1q} & n_{x_1}\newline
\vdots & \vdots & \ddots & \vdots & \ddots & \vdots & \vdots \newline
x_i & n_{i1} & \cdots & n_{ij} & \cdots & n_{iq} & n_{x_i}\newline
\vdots & \vdots & \ddots & \vdots & \ddots & \vdots & \vdots\newline
x_p & n_{p1} & \cdots & n_{pj} & \cdots & n_{pq} & n_{x_p} \newline
\hline
n_y & n_{y_1} & \cdots & n_{y_j} & \cdots & n_{y_q} & n\newline
\hline
\end{array}
$$

si $X$ e $Y$ fuesen independientes, para cualquier valor $y_j$ se tendría

$$\frac{n_{1j}}{n_{x_1}} = \frac{n_{2j}}{n_{x_2}} = \cdots = \frac{n_{pj}}{n_{x_p}} = \frac{n_{1j}+\cdots
+n_{pj}}{n_{x_1}+\cdots+n_{x_p}} = \frac{n_{y_j}}{n},$$ de donde se deduce que $$n_{ij} = \frac{n_{x_i}n_{y_j}}{n}.$$

A esta última expresión se le llama _frecuencia teórica_ o _frecuencia esperada_ del par $(x_i,y_j)$.

### Coeficiente chi-cuadrado $\chi^2$

Es posible estudiar la relación entre dos atributos $X$ e $Y$ comparando las frecuencias reales con las esperadas:

{{% alert def %}}
**Definición - Coeficiente Chi-cuadrado $\chi^2$**. Dada una muestra de tamaño $n$ en la que se han medido dos atributos $X$ e $Y$, se define el coeficiente $\chi^2$ como

$$\chi^2 = \sum_{i=1}^p\sum_{j=1}^q \frac{\left(n_{ij}-\frac{n_{x_i}n_{y_j}}{n}\right)^2}{\frac{n_{x_i}n_{y_j}}{n}},$$

donde $p$ es el número de categorías de $X$ y $q$ el número de categorías de $Y$.
{{% /alert %}}

{{% alert warning %}}
Por ser suma de cuadrados, se cumple que

$$\chi^2 \geq 0.$$
{{% /alert %}}

{{% alert int %}}
$\chi^2=0$ cuando los atributos son independientes, y crece a medida que aumenta la dependencia entre las variables.
{{% /alert %}}

**Ejemplo**. Siguiendo con el ejemplo anterior, a partir de la tabla de contingencia

$$
\begin{array}{|l|rr|r|}
\hline
\text{Sexo}\backslash\text{Fuma} & \text{Si} & \text{No} & n_i\newline
\hline
\text{Mujer} & 12 & 28 & 40 \newline
\text{Hombre} & 26 & 34 & 60 \newline
\hline
n_j & 38 & 62 & 100\newline
\hline
\end{array}
$$

se obtienen las siguientes frecuencias esperadas

$$
\renewcommand{\arraystretch}{1.5}
\begin{array}{|l|rr|r|}
\hline
\mbox{Sexo\backslash Fuma} & \mbox{Si} & \mbox{No} & n_i\newline
\hline
\text{Mujer} & \frac{40\cdot 38}{100}=15.2 & \frac{40\cdot 62}{100}=24.8 & 40 \newline
\text{Hombre} & \frac{60\cdot 38}{100}=22.8 & \frac{60\cdot 62}{100}=37.2 & 60 \newline
\hline
n_j & 38 & 62 & 100\newline
\hline
\end{array}
$$

y el coeficiente $\chi^2$ vale

$$\chi^2 = \frac{(12-15.2)^2}{15.2}+\frac{(28-24.8)^2}{24.8}+\frac{(26-22.8)^2}{22.8}+\frac{(34-37.2)^2}{37.2} = 1.81.$$

Esto indica que no existe gran relación entre el sexo y el hábito de fumar.

### Coeficiente de contingencia

El coeficiente $\chi^2$ depende del tamaño muestral, ya que al multiplicar por una constante las frecuencias de todas las casillas, su valor queda multiplicado por dicha constante, lo que podría llevarnos al equívoco de pensar que ha aumentado la relación, incluso cuando las proporciones se mantienen. En consecuencia el valor de $\chi^2$ no está acotado superiormente y resulta difícil de interpretar.

Para evitar estos problemas se suele utilizar el siguiente estadístico.

{{% alert def %}}
**Definición - Coeficiente de contingencia**. Dada una muestra de tamaño $n$ en la que se han medido dos atributos $X$ e $Y$, se define el _coeficiente de contingencia_ como

$$C = \sqrt{\frac{\chi^2}{\chi^2+n}}$$
{{% /alert %}}

{{% alert warning %}}
De la definición anterior se deduce que

$$0\leq C\leq 1,$$
{{% /alert %}}

{{% alert int %}}
$C=0$ cuando las variables son independientes, y crece a medida que aumenta la relación.
{{% /alert %}}

{{% alert warning %}}
Aunque $C$ nunca puede llegar a valer 1, se puede demostrar que para tablas de contingencia con $k$ filas y $k$ columnas, el valor máximo que puede alcanzar $C$ es $\sqrt{(k-1)/k}$.
{{% /alert %}}

**Ejemplo**. En el ejemplo anterior el coeficiente de contingencia vale

$$C = \sqrt{\frac{1.81}{1.81+100}} = 0.13.$$

Como se trata de una tabla de contingencia de $2\times 2$, el valor máximo que podría tomar el coeficiente de contingencia es $\sqrt{(2-1)/2}=\sqrt{1/2}=0.707$, y como $0.13$ está bastante lejos de este valor, se puede concluir que no existe demasiada relación entre el hábito de fumar y el sexo.
