---
title: Examen de Fisioterapia 2018-05-31
date: 2018-05-31
tags: [Examen]
categories: [Estadística, Bioestadística, Fisioterapia]
type: book
---

Grados: Fisioterapia  
Fecha: 31 de mayo de 2018

## Ejercicio 1

Las edades de una muestra de pacientes que acuden a una clínica de fisioterapia son las siguientes:

25, 30, 44, 44, 51, 51, 53, 56, 57, 58, 58, 58, 59, 59, 61, 63, 63, 63, 66, 68, 70, 71, 72, 74, 82, 85

Se pide:

1. Calcular los cuartiles.
2. Dibujar el diagrama de cajas e identificar los datos atípicos (no agrupar los datos en intervalos).
3. Considerando los grupos de los menores y mayores de 65 años, ¿en cuál de ellos es más representativa la media?
4. ¿Qué distribución es menos simétrica, la de los menores o la de los mayores de 65 años?
5. ¿Qué edad es relativamente mayor con respecto a su grupo, 50 años en el grupo de los menores o 75 en el de los mayores?

Usar las siguientes sumas para los cálculos.  
Menores de 65: $\sum x_i=953$ años, $\sum x_i^2=52475$ años$^2$, $\sum (x_i-\bar x)^3=-30846.51$ años$^3$ y $\sum (x_i-\bar x)^4=939658.83$ años$^4$.  
Mayores de 65: $\sum x_i=588$ años, $\sum x_i^2=43530$ años$^2$, $\sum (x_i-\bar x)^3=1485$ años$^3$ y $\sum (x_i-\bar x)^4=26983.5$ años$^4$.

{{< spoiler text="Solución" >}}

1. $C_1=53$ años, $C_2=59$ años and $C_3=68$ años.  
2. Existen dos datos atípicos: 25 y 30.  
<img src="../img/des-fis-1-diagrama-caja-edades.svg" title="Diagrama de caja de edades" alt="Diagrama de caja de edades de pacientes" width="600" />
3. Sea $X$ la edad de los pacientes menores de 65 años e $Y$ la de los mayores.  
$\bar x=52.9444$ años, $s_x^2=112.1636$ años$^2$, $s_x=10.5907$ años y $cv_x=0.2$.  
$\bar y=73.5$ años, $s_y^2=39$ años$^2$, $s_y=6.245$ años y $cv_y=0.085$.  
La media es más representativa en los pacientes mayores de 65 ya que el coeficiente de variación es menor.
4. $g_{1x}=-1.4426$ y $g_{1y}=0.7621$, de manera que la distribución menos simétrica es la de los menores de 65 años.
5. Las puntuaciones típicas son $z_x(50)=-0.278$ y $z_y(72)=-0.2402$, de manera que una edad de 50 años es relativamente menor en el grupo de los menores de 65 años.
{{< /spoiler >}}

## Ejercicio 2

La siguiente tabla recoge el número de lesiones en un equipo durante una temporada y el número medio de minutos diarios de calentamiento que hacen sus jugadores.

$$
\begin{array}{lrrrrrrrrrr}
\hline
\mbox{Tiempo calentamiento} & 15 & 35 & 22 & 28 & 21 & 18 & 25 & 30 & 23 & 20 \newline
\mbox{Lesiones} & 42 & 2 & 16 & 6 & 17 & 29 & 10 & 3 & 12 & 20 \newline
\hline
\end{array}
$$

Se pide:

1. Dibujar el diagrama de dispersión.
2. ¿Qué modelo de regresión es más apropiado para predecir el número de lesiones en función del tiempo de calentamiento, el logarítmico o el exponencial? Utilizar dicho modelo para predecir el número de lesiones esperado para 20 minutos de calentamiento diarios.
3. ¿Qué modelo de regresión es más apropiado para predecir el tiempo de calentamiento en función del número de lesiones, el logarítmico o el exponencial? Utilizar dicho modelo para predecir el mínimo tiempo de calentamiento diario necesario para no tener más de 10 lesiones en la temporada.
4. ¿Son fiables estas predicciones? ¿Cuál de ellas es más fiable?

Usar las siguientes sumas para los cálculos (X=tiempo de calentamiento e Y=número de lesiones):
$\sum x_i=237$, $\sum \log(x_i)=31.3728$, $\sum y_j=157$, $\sum \log(y_j)=24.0775$,  
$\sum x_i^2=5937$, $\sum \log(x_i)^2=98.9906$, $\sum y_j^2=3843$, $\sum \log(y_j)^2=66.3721$,  
$\sum x_iy_j=3115$, $\sum x_i\log(y_j)=519.1907$, $\sum \log(x_i)y_j=465.8093$, $\sum \log(x_i)\log(y_j)=73.3995$.

{{< spoiler text="Solución" >}}
1. <img src="../img/des-fis-5-poligono-frecuencias-relativas-acumuladas-lesiones-vertebrales.svg" title="Diagrama de dispersión de lesiones vs tiempo de calentamiento" alt="Diagrama de dispersión de lesiones vs tiempo de calentamiento" width="600" />  
2. $\bar x=23.7$ min, $s_x^2=32.01$ min$^2$.  
$\overline{\log(x)}=3.1373$ log(min), $s_{\log(x)}^2=0.0565$ log(min)$^2$.  
$\bar y=15.7$ lesiones, $s_y^2=137.81$ lesiones$^2$.  
$\overline{\log(y)}=2.4078$ log(lesiones), $s_{\log(y)}^2=0.8399$ log(lesiones)$^2$.  
$s_{x\log(y)}=-5.1446$, $s_{\log(x)y}=-2.6744$  
Coeficiente de determinanción exponencial: $r^2=0.9844$  
Coeficiente de determinación logarítmico: $r^2=0.9185$  
Por tanto, el modelo de regresión exponencial es mejor para predecir el número de lesiones en función del tiempo de
calentamiento.  
Modelo de regresión exponencial: $y=e^{6.2168+-0.1607x}$.  
Predicción: $y(20)=20.1341$ lesiones.  
3. El modelo logarítmico es mejor para predecir el tiempo de calentamiento en función del número de lesiones.  
Modelo de regresión logarítmico: $x=164.1851+-47.3292\log(y)$.  
Predicción: $x(10)=55.2056$ min.  
4. De acuerdo al coeficiente de determinación ambas predicciones son muy fiables pero la última lo es menos ya que es para un valor que no está incluido en el rango de valores de la muestra.
{{< /spoiler >}}

## Ejercicio 3

Se recurre a cierta técnica con ultrasonidos en el proceso de diagnosis de una enfermedad.
Su sensibilidad es del 91% y su especificidad del 98%.
Sabiendo que la prevalencia de dicha enfermedad es del 20%, se pide:

1. Si a un individuo se le aplica la técnica y el resultado es positivo, ¿cuál es la probabilidad de que sufra esta enfermedad?
2. Si el resultado fuese negativo, ¿cuál sería la probabilidad de que no tuviera la enfermedad?
3. ¿La técnica es más fiable para confirmar la enfermedad o para descartarla? Justificar la respuesta.
4. Calcular la probabilidad de obtener un diagnóstico acertado con esta técnica.

{{< spoiler text="Solución" >}}
Sea $E​$ el suceso consistente en tener la enfermedad y $+​$ y $-​$ los sucesos correspondientes a obtener un resultado positivo y negativo respectivamente en el test.

1. $VPP=0.9192$.
2. $VPN=0.9776$.
3. Es más fiable para descartar la enfermedad ya que el valor predictivo negativo es mayor que el valor predictivo positivo.
4. $P(E\cap +)+P(\overline E\cap -) = 0.966$.
{{< /spoiler >}}

## Ejercicio 4

Se sabe que la longitud del fémur de un feto a las 25 semanas de embarazo sigue una distribución normal de media 44 mm y desviación típica 2 mm.
Se pide:

1. Calcular la probabilidad de que, tomando un feto de 25 semanas al azar, el fémur mida más de 46 mm.
2. Calcular la probabilidad de que, tomando un feto de 25 semanas al azar, el fémur mida entre 46 y 49 mm.
3. Determina un intervalo $(a,b)$ centrado en la media, que contenga el 80% de los valores de la longitud del fémur de fetos de 25 semanas.

{{< spoiler text="Solución" >}}
Sea $X\sim N(44,2)$ la longitud del fémur de un feto a las 25 semanas de embarazo.  

1. $P(X>46)=0.1587$.
2. $P(46<X<49)=0.1524$.
3. El intervalo centrado en $44$ que contiene 80% de las longitudes del fémur de fetos de 25 semanas es $(41.4369,46.5631)$.
{{< /spoiler >}}

## Ejercicio 5

La probabilidad de que una lesión $A$ se reproduzca es $4/5$, la de que se reproduzca otra lesión $B$ es $1/2$, y la de que ninguna se reproduzca $1/20$. 
Hallar la probabilidad de que:

1. Al menos una se reproduzca.
2. Sólo se reproduzca la lesión $B$.
3. Se reproduzca la lesión $B$ si se ha reproducido la $A$.
4. Se reproduzca la lesión $B$ si no se reproduce la lesión $A$.

{{< spoiler text="Solución" >}}

1. $P(A\cup B)=19/20$.
2. $P(B\cap\overline{A})=3/20$.
3. $P(B/A)=7/16$.
4. $P(B/\overline{A})=3/4$.
{{< /spoiler >}}

## Ejercicio 6

Una clínica de fisioterapia abre 6 horas al día y se sabe que el número medio de pacientes por día que llegan a la clínica es 12.
Se pide:

1. Calcular la probabilidad de que lleguen más de 4 pacientes en 1 horas.
2. Si la clínica tiene 4 fisioterapeutas y cada uno puede atender a un paciente por hora, ¿cuál es la probabilidad de que un día cualquiera haya alguna hora en la que algún paciente no pueda ser atendido? ¿Cuántos empleados debería haber para asegurarse de que esta probabilidad es menor del 10%?

{{< spoiler text="Solución" >}}

1. Sea $X$ el número de pacientes que llegan en 1 horas. $X\sim P(2)$ y $P(X>4)=0.0527$.
2. Sea $Y$ el número de horas en un día en las que algún paciente no puede ser atendido. $Y\sim B(6, 0.0527)$ y $P(Y>0)=0.2771$.  
Se necesitan 5 empleados para que esta probabilidad sea menor del 10%, ya que $P(X>5)=0.0527$ y $P(Y>0)=0.0954$, siendo ahora $Y\sim B(6, 0.0166)$.
{{< /spoiler >}}
