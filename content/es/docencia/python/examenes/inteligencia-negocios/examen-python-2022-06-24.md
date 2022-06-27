---
title: Examen de Inteligencia de los Negocios 2022-06-24
date: 2022-06-24
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 24 de junio de 2022

## Ejercicio 1

Las matemáticas financieras, resumidas en una frase, las podríamos definir como la rama de las matemáticas que estudia los flujos de dinero a través del tiempo. Básicamente se presupone que el dinero tiene menos valor en el futuro que en el presente, ya sea por un tema inflacionario o por la preferencia natural de las personas a priorizar el consumo presente. 

El valor futuro es el valor alcanzado por un determinado capital al final del período determinado (para el ejemplo usaremos la fórmula del interés compuesto). Para calcularlo se utiliza la siguiente fórmula

$$VF = VA\cdot (1 + i)^n$$

El valor presente de una inversión es cuando calculamos el valor actual que tendrá una determinada cantidad que recibiremos o pagaremos en un futuro. Para calcularlo se utiliza la siguiente fórmula

$$VA = \frac{VF}{(1 + i)^n}$$

Donde $VF$ es el valor futuro, $VA$ es el valor actual o inicial de la inversión, $i$ es el tipo de interés y $n$ es número de años de la inversión.

1. Crear una función que reciba como entrada un capital, un tipo de interés y un número de años, y muestre por pantalla el valor futuro de la inversión cada año del periodo indicado.
2. Crear una función que reciba como entrada un capital, un tipo de interés y un número de años, y muestre por pantalla el valor actual del capital cada año del periodo indicado.

**Ejemplo de ejecución**

```sh
Introduce un capital: 1000
Introduce un tipo de interés: 10
Introduce un número de años: 3
VALOR FUTURO
Año 0 : 1100.0
Año 1 : 1210.0000000000002
Año 2 : 1331.0000000000005
VALOR ACTUAL
Año 0 : 909.090909090909
Año -1 : 826.4462809917354
Año -2 : 751.3148009015775
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-24/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Realizar un programa que simule el juego de las tres en raya. Cada jugador solo debe colocar su ficha una vez por turno y no debe ser sobre una casilla ya ocupada. En caso de que el jugador haga trampa el ganador será el otro. Para ganar se debe conseguir realizar una línea recta (horizontal, vertical o diagonal) con la misma ficha. El tablero es de 3x3 y cualquier casilla podrá estar vacía u ocupada sólo por una ficha X o 0. El programa debe realizar las siguientes operaciones:

- Mostrar el tablero por pantalla.
- Poner una ficha en una cuadricula comprobando que no está ocupada.
- Comprobar si se produce tres en raya e indicar si es de X o de O, o si hay empate.

**Ejemplo de ejecución**

```sh
[' ', ' ', ' ']
[' ', ' ', ' ']
[' ', ' ', ' ']
Introduce la coordenada X del 1 al 3: 2
Introduce la coordenada Y del 1 al 3: 2
Introduce 0 para círculo o X para cruz: X
[' ', ' ', ' ']
[' ', 'X', ' ']
[' ', ' ', ' ']
Introduce la coordenada X del 1 al 3: 2
Introduce la coordenada Y del 1 al 3: 1
Introduce 0 para círculo o X para cruz: 0
[' ', ' ', ' ']
['0', 'X', ' ']
[' ', ' ', ' ']
Introduce la coordenada X del 1 al 3: 2
Introduce la coordenada Y del 1 al 3: 1
Introduce 0 para círculo o X para cruz: X
Esa coordenada ya está siendo utilizada, use una libre.
[' ', ' ', ' ']
['0', 'X', ' ']
[' ', ' ', ' ']
Introduce la coordenada X del 1 al 3: 3
Introduce la coordenada Y del 1 al 3: 1
Introduce 0 para círculo o X para cruz: X
[' ', ' ', ' ']
['0', 'X', ' ']
['X', ' ', ' ']
Introduce la coordenada X del 1 al 3: 1
Introduce la coordenada Y del 1 al 3: 2
Introduce 0 para círculo o X para cruz: 0
[' ', '0', ' ']
['0', 'X', ' ']
['X', ' ', ' ']
Introduce la coordenada X del 1 al 3: 1
Introduce la coordenada Y del 1 al 3: 3
Introduce 0 para círculo o X para cruz: X
[' ', '0', 'X']
['0', 'X', ' ']
['X', ' ', ' ']
La partida la ha ganado el jugador con la ficha X.
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-24/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

El fichero [bank-loans.csv](https://aprendeconalf.es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-24/bank-loans.csv) contiene información sobre los préstamos de los clientes de un banco. Utilizando la librería Pandas, se pide:  

- Crear un DataFrame importando los datos del fichero.
- Mostrar por pantalla el nombre de las columnas del DataFrame. 
- Mostrar por pantalla las filas del DataFrame múltiplos de 10. 
- Mostrar por pantalla el número de clientes casados con edad entre 30 y 40 años. 
- Añadir al DataFrame una columna nueva con la edad en meses. 
- Mostrar por pantalla las frecuencias de los oficios ordenadas de mayor a menor. 
- Mostrar por pantalla las edades medias según el nivel de estudios. 
- Mostrar por pantalla el porcentaje de préstamos hipotecarios (housing) según el estado civil (marital). 
- Dibujar el diagrama de sectores con los porcentajes de los niveles de estudio y ponerle un título. 
- Dibujar en una misma figura el histograma y el diagrama de cajas de las edades. El histograma debe tener clases de amplitud 10 desde 20 hasta 70 años, y en color rojo.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-24/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 4

El fichero [bank-loans.csv](https://aprendeconalf.es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-24/bank-loans.csv) contiene información sobre los préstamos de los clientes de un banco. Utilizando ficheros (sin usar la librería Pandas), crear una función que tenga como parámetros la url del fichero, el nombre de una columna cualitativa y un booleano para los porcentajes (False por defecto), que devuelva un diccionario con las frecuencias absolutas de las categorías de la columna indicada. Si se pasa True como argumento del parámetro para el porcentaje, la función debe devolver el diccionario de porcentajes de las categorías. 


**Ejemplo de ejecución**

Salida de la llamada a la función con la columna "education".

```sh
{'basic.4y': 1299, 'high.school': 2382, 'basic.6y': 761, 'basic.9y': 1820, 'professional.course': 1142, 'unknown': 485, 'university.degree': 2109, 'illiterate': 2}
```

Salida de la llamada a la función con la columna "housing" y porcentaje = `True`.

```sh
{'no': 51.88, 'yes': 45.24, 'unknown': 2.88}
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-24/ejercicio4.ipynb" class="btn btn-info" target="_blank">Solución</a>