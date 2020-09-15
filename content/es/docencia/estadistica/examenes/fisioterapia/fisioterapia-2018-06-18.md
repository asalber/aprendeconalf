---
title: Examen de Fisioterapia 2018-06-18
date: 2018-06-18
tags: [Examen]
categories: [Estadística, Bioestadística, Fisioterapia]
type: book
---

Grados: Fisioterapia  
Fecha: 18 de junio de 2019

## Ejercicio 1

En un estudio sobre la efectividad de un programa de prevención de riesgos laborales en oficios que requieren estar sentados muchas horas, se tomó una muestra aleatoria de individuos entre 40 y 50 años que pasaban más de 5 horas sentados y se observó si habían seguido las recomendaciones del programa de prevención o no y el número de lesiones vertebrales transcurridos 10 años. 
Los resultados obtenidos aparecen en la siguiente tabla.

$$
\begin{array}{lrrrrrrrrrrrrrrr}
\hline
\mbox{Con programa de prevención} & 1 & 3 & 2 & 4 & 4 & 0 & 2 & 4 & 2 & 2 & 5 & 2 & 3 & 2 & 0 \newline
\mbox{Sin programa de prevención} & 6 & 3 & 1 & 3 & 7 & 6 & 5 & 5 & 9 & 5 & 5 & 4 & 4 & 3 &  \newline
\hline
\end{array}$$

Se pide:

1. Dibujar el polígono de frecuencias relativas acumuladas de la muestra global.
2. Según el rango intercuartílico, ¿en qué muestra hay una mayor dispersión central del número de lesiones vertebrales, en la de los que siguieron el programa de prevención o en la de los que no?
3. ¿En qué muestra hay una mayor dispersión relativa del número de lesiones vertebrales, en la de los que siguieron el programa de prevención o en la de los que no?
4. ¿Qué muestra tienen un apuntamiento más normal del número de lesiones vertebrales, la de los que siguieron el programa de prevención o en la de los que no?
5. ¿Qué número de lesiones vertebrales es relativamente mayor, 2 lesiones siguiendo el programa de prevención o 4 sin seguirlo?

Usar las siguientes sumas para los cálculos:  
Siguiendo el programa de prevención: $\sum x_i=36$ lesiones, $\sum x_i^2=116$ lesiones$^2$, $\sum (x_i-\bar x)^3=-0.48$ lesiones$^3$ y $\sum (x_i-\bar x)^4=135.97$ lesiones$^4$.  
No siguiendo el programa de prevención: $\sum y_i=66$ lesiones, $\sum y_i^2=362$ lesiones$^2$, $\sum (y_i-\bar y)^3=27.92$ lesiones$^3$ y $\sum (y_i-\bar y)^4=586.9$ lesiones$^4$.

{{< spoiler text="Solución" >}}
1. <img src="../img/des-fis-5-poligono-frecuencias-relativas-acumuladas-lesiones-vertebrales.svg" title="Cumulative relative frequency polygon of spinal injuries" alt="Cumulative relative frequency polygon of spinal injuries" style="display: block; margin: auto;" width="600" />
  
2. Con programa de prevención: $C_1=2$ lesiones, $C_3=4$ lesiones, $RI=2$ lesiones.  
Sin programa de prevención: $C_1=3$ lesiones, $C_3=6$ lesiones, $RI=3$ lesiones.  
La muestra que no siguió el programa de prevención tiene una dispersión central mayor ya que su rango intercuartílico es mayor.

3. Con programa de prevención: $\bar x=2.4$ lesiones, $s^2=1.9733$ lesiones$^2$, $s=1.4048$ lesiones and $cv=0.5853$.  
Sin programa de prevención: $\bar y=4.7143$ lesiones, $s^2=3.6327$ lesiones$^2$, $s=1.906$ lesiones and $cv=0.4043$.  
La muestra que siguió el programa de prevención tiene una dispersión relativa con respecto a la media mayor ya que su coeficiente de variación es mayor.

4. Con programa de prevención: $g_2=-0.6722$.  
Sin programa de prevención: $g_2=0.1768$.  
Así pues, la muestra que no siguió el programa de prevención tiene un apuntamiento más normal ya que el coeficiente de apuntamiento está más próximo a 0.

5. Con programa de prevención: $z(2)=-0.2847$.  
Sin programa de prevención: $z(4)=-0.3748$.  
Así pues, 4 lesiones sin seguir el programa de prevención es relativamente menor que 2 lesiones siguiendo el programa ya que su puntuación típica es menor.
{{< /spoiler >}}

## Ejercicio 2

El precio de cierto relajante muscular evolucionó entre 2015 y 2019
como indica la siguiente tabla:

$$
\begin{array}{lrrrrr}
\hline
\mbox{Año} & 2015 & 2016 & 2017 & 2018 & 2019 \newline
\mbox{Precio (€)} & 1.40 & 1.60 & 1.92 & 2.30 & 2.91 \newline
\hline
\end{array}
$$

1. ¿Qué modelo de regresión es mejor para predecir el precio del función del año, el lineal o el exponencial?
2. Utilizar el mejor de los dos modelos anteriores para predecir el precio del medicamento en 2020.

{{< spoiler text="Solución" >}}

1. $\bar x=2017$ años, $s_x^2=2$ años$^2$.  
$\bar y=2.026$ €, $s_y^2=0.2882$ €$^2$.  
$\overline{\log(y)}=0.672$ log(€), $s_{\log(y)}^2=0.0673$ log(€)$^2$.  
$s_{xy}=0.744$ años$\cdot$€, $s_{x\log(y)}=0.3653$ años$\cdot\log(€)$.  
Coeficiente de determinación lineal: $r^2=0.9603$.  
Coeficiente de determinación exponencial: $r^2=0.9909$.  
Así pues, el modelo de regresión exponencial es mejor para predecir el precio ya que su coeficiente de determinación es mayor.  

2. Modelo de regresión exponencial: $y=e^{-367.6861+0.1826x}$.  
Predicción: $y(2020)=3.3867$ €.
{{< /spoiler >}}

## Ejercicio 3

En un problema de regresión lineal entre dos variables $X$ e $Y$ se conoce $\bar x = 3$, $s_x^2=2$, $s_y^2=10.8$ y la ecuación de la recta de regresión de $Y$ sobre $X$ es $y=90.9-2.3x$.

1. Calcular la media de $Y$.
2. Calcular e interpretar el coeficiente de correlación lineal.

{{< spoiler text="Solución" >}}

1. $\bar y = 84$.  
2. $r=-0.9898$.
{{< /spoiler >}}

## Ejercicio 4

En un estudio sobre la efectividad de un programa de prevención de riesgos laborales en oficios que requieren estar sentados muchas horas, se tomó una muestra aleatoria 500 de individuos entre 40 y 50 años sin lesiones vertebrales que pasaban más de 5 horas sentados.
La mitad de los individuos siguieron un programa de prevención de riesgos laborales mientras que los demás no.
Transcurridos 5 años el número de personas que desarrollaron alguna lesión vertebral en el grupo de los que siguieron el programa de prevención fue de 12, mientras que en el otro grupo fue de 32.
En los siguientes 5 años hubo otras 21 personas que desarrollaron alguna lesión vertebral en el grupo de los que siguieron el programa de prevención, mientras que en el otro grupo fue de 48.

1. Calcular la incidencia acumulada de lesiones vertebrales en la muestra total a los 5 y a los 10 años.
2. Calcular el riesgo absoluto de desarrollar alguna lesión vertebral a los 10 años en el grupo de los que siguieron el programa de prevención y en el de los que no.
3. Calcular el riesgo relativo de desarrollar alguna lesión vertebral a los 10 años de los que siguieron el programa de prevención de riesgos con respecto a los que no e interpretarlo.
4. Calcular el odds ratio de desarrollar alguna lesión vertebral a los 10 años de los que siguieron el programa de prevención de riesgos con respecto a los que no e interpretarlo.
5. ¿Cuál de las dos medidas anteriores, riesgo relativo u odds ratio, tiene más sentido en este estudio?
Justificar la respuesta.

{{< spoiler text="Solución" >}}
Sea $E$ el evento consistente en sufrir una lesión vertebral.  

1. Incidencia acumulada después de 5 años: $R(E)=0.088$.  
Incidencia acumulada después de 10 años: $R(E)=0.226$.

2. Riesgo en el grupo tratamiento: $R_T(E)=0.132$.  
Riesgo en el grupo control: $R_C(E)=0.32$.

3. $RR(D)=0.4125$. Por tanto, el riesgo de sufrir una lesión vertebral es menos de la mitad si se sigue el programa de prevención.

4. $OR(D)=0.3232$. Por tanto, el odd de sufrir una lesión vertebral es menos de un tercio si se sigue el programa de prevención.

5. Puesto que se trata de un estudio prospectivo se puede estimar la prevalencia de $D$ y ambos estadísticos son válidos, pero el riesgo relativo es más fácil de interpretar.
{{< /spoiler >}}

## Ejercicio 5

En la siguiente tabla se muestran los resultados de un estudio para evaluar la utilidad de una tira reactiva para el diagnóstico de infección urinaria: 

$$\begin{array}{ccc}
\hline
\mbox{Resultado} & \mbox{Con infección} & \mbox{Sin infección}\newline
\mbox{Positivo} & 60 & 80\newline
\mbox{Negativo} & 10 & 200\newline
\hline
\end{array}
$$

1. Calcular la sensibilidad y la especificidad del test.
2. Calcular los valores predictivos positivo y negativo del test.
¿El test es mejor para confirmar la enfermedad o para descartarla?
3. Si a partir de un estudio de prevalencia efectuado previamente conociéramos que la verdadera prevalencia de la infección urinaria en la población es del 2%, ¿cómo se verían afectados los valores predictivos?

{{< spoiler text="Solución" >}}
Sea $E$ el suceso consistente en tener la infección urinaria y $+$ y $-$ los sucesos correspondientes a obtener un resultado positivo y negativo respectivamente en el test.  

1. Sensibilidad = $0.8571$ y Especificidad = $0.7143$.
2. $VPP=0.4286$ y $VPN=0.9524$. Puesto que $VPP<VPN$ el test es mejor para descartar la enfermedad.
3. $VPP=0.0577$ y $VPN=0.9959$. El valor predictivo positivo decrece mucho mientras el valor predictivo negativo aumenta un poco.
{{< /spoiler >}}

## Ejercicio 6

El tiempo de recuperación tras un tipo de lesión sigue una distribución normal con varianza 64 días. Se sabe además que el 10% de las personas con esta lesión tardan en curarse más de 80 días.

1. ¿Cuál es el tiempo esperado de curación para esta lesión?
2. ¿Qué porcentaje de individuos tardará en curarse entre 60 y 75 días?
3. Si se toma una muestra aleatoria de 12 individuos con esta lesión, ¿cuál es la probabilidad de que haya entre 9 y 11 individuos, ambos incluidos, que tarden menos de 80 días en curarse?
4. Si se toma una muestra aleatoria de 500 individuos con esta lesión, ¿cuál es la probabilidad de haya menos de 4 por encima del percentil 99 del tiempo de curación?

{{< spoiler text="Solución" >}}
Sea $X$ el tiempo requerido para recuperarse de la lesión.
Entonces $X\sim N(\mu, 8)$.  

1. $\mu=69.7476$ días.
2. $P(60<X<75) = 0.6327$.
3. Sea $Y$ el número de individuos con la lesión que requieren más de 80 días para recuperarse en una muestra aleatoria de 12 individuos. Entonces $Y\sim B(12, 0.9)$ y $P(9\leq Y\leq 11)=0.6919$.  
4. Sea $Z$ be el número de individuos con la lesión que requieren un tiempo de recuperación por encima del percentil 99 en una muestra aleatoria de 500 individuos. Entonces $Z\sim B(500, 0.01)\approx P(5)$ y $P(Z\leq 4)=0.265$.
{{< /spoiler >}}
