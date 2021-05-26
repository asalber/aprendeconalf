---
title: Examen de Inteligencia de los Negocios 2021-05-26
date: 2021-05-26
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 26 de mayo de 2021

## Ejercicio 1

Dadas dos listas de números del mismo tamaño `x` e `y`, construir las siguientes funciones:

1. Una función para calcular la media de una lista de números.
2. Una función para calcular la varianza de una lista de números.
3. Una función para calcular la covarianza de dos listas de números.
4. Una función para calcular los coeficientes de la recta de regresión de `y` sobre `x`.
5. Una función que devuelva el diagrama de dispersión y la recta de regresión como la que se muestra en el siguiente ejemplo:

```pyhton
x = [1, 2, 3, 4, 5, 6]
y = [20, 18, 12, 10, 9, 9]
```

!['Recta de regresión'](../img/recta-regresion.png)

Usar las siguientes fórmulas para el cálculo de los estadísticos: $\bar x = \frac{\sum x_i}{n}$, $s^2 = \frac{\sum x_i^2}{n}-\bar{x}^2$, $s_{xy} = \frac{\sum x_iy_j}{n} - \bar{x}\bar{y}$, $b = \frac{s_{xy}}{s_x^2}$ y $a = \bar{y} - b * \bar{x}$.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-05-26/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Escribir una función que, dado un número `x`, genere una matriz cuadrada (`x*x` elementos) con el resultado de sus tablas de multiplicar desde 0 hasta `x`. El resultado debe guardarse en un fichero llamado `tabla-X.txt` donde `X` es el número introducido por el usuario.

Escribir otra función que, dado un número `x`, acceda al fichero de la tabla correspondiente y muestre la tabla por pantalla. En caso de que la tabla no exista deberá controlar la excepción para mostrar un mensaje de aviso al usuario.

Ejemplo:

```sh
>>> Introduce un número entre 1 y 10: 5
>>> Contenido del fichero matriz-5.txt
0    0    0    0    0    0
0    1    2    3    4    5
0    2    4    6    8    10
0    3    6    9    12   15
0    4    8    12   16   20
0    5    10   15   20   25
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-05-26/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Crear un programa utilizando la librería Pandas y Matplotlib que realice lo siguiente:

1. Crear el siguiente DataFrame indexado:
    ```sh
      calorias  tiempo
    L      420      60
    M      380      40
    X      390      75
    J      490      55
    V      300      45
    ```
2. Calcular la media, mediana y desviación típica de ambas columnas.
3. Añadir otra columna booleana al DataFrame para ver si se ha cumplido el reto de quemar más de 400 calorías por hora. La nueva columna debe generarse aplicando una fórmula a las otras columnas. El DataFrame resultante debe ser el siguiente:
    ```sh
      calorias  tiempo   reto
    L      420      60   True
    M      380      40   True
    X      390      75  False
    J      490      55   True
    V      300      45  False
    ```
4. Filtrar el DataFrame y devolver otro DataFrame con las filas pares que cumplan que el número de calorías es mayor de 400.
5. Crear a partir del DataFrame una serie con los porcentajes de días que se ha conseguido el reto y los que no.
6. Crear un gráfico como el de más abajo que muestre la progresión de las calorías y tiempo durante la semana.

![Serie evolución calorias](../img/evolucion-calorias.png)

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-05-26/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>
