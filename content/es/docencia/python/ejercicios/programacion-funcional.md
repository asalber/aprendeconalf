---
title: Ejercicios de Programación Funcional
linkTitle: Programación Funcional
date: 
lastmod:
tags: [Ejercicios, Programación Funcional]
categories: [Programación, Python]
type: book
weight: 70
---

## Ejercicio 1

Escribir una función que aplique un descuento a un precio y otra que aplique el IVA a un precio. Escribir una tercera función que reciba un diccionario con los precios y porcentajes de una cesta de la compra, y una de las funciones anteriores, y utilice la función pasada para aplicar los descuentos o el IVA a los productos de la cesta y devolver el precio final de la cesta.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio1.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 2

Escribir una función que simule una calculadora científica que permita calcular el seno, coseno, tangente, exponencial y logaritmo neperiano. La función preguntará al usuario el valor y la función a aplicar, y mostrará por pantalla una tabla con los enteros de 1 al valor introducido y el resultado de aplicar la función a esos enteros.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio2.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 3

Escribir una función que reciba otra función y una lista, y devuelva otra lista con el resultado de aplicar la función dada a cada uno de los elementos de la lista.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio3.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 4

Escribir una función que reciba otra función booleana y una lista, y devuelva otra lista con los elementos de la lista que devuelvan `True` al aplicarles la función booleana.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio4.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 5

Escribir una función que reciba una frase y devuelva un diccionario con las palabras que contiene y su longitud.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio5.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 6

Escribir una función reciba una lista de notas y devuelva la lista de calificaciones correspondientes a esas notas.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio6.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 7

Escribir una función reciba un diccionario con las asignaturas y las notas de un alumno y devuelva otro diccionario con las asignaturas en mayúsculas y las calificaciones correspondientes a las notas.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio7.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 8

Escribir una función reciba un diccionario con las asignaturas y las notas de un alumno y devuelva otro diccionario con las asignaturas en mayúsculas y las calificaciones correspondientes a las notas aprobadas.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio8.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 9

Escribir una función que calcule el módulo de un vector.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio9.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 10

Una inmobiliaria de una ciudad maneja una lista de inmuebles como la siguiente:

```python
[{'año': 2000, 'metros': 100, 'habitaciones': 3, 'garaje': True, 'zona': 'A'},
{'año': 2012, 'metros': 60, 'habitaciones': 2, 'garaje': True, 'zona': 'B'},
{'año': 1980, 'metros': 120, 'habitaciones': 4, 'garaje': False, 'zona': 'A'},
{'año': 2005, 'metros': 75, 'habitaciones': 3, 'garaje': True, 'zona': 'B'},
{'año': 2015, 'metros': 90, 'habitaciones': 2, 'garaje': False, 'zona': 'A'}]
```

Construir una función que permita hacer búsqueda de inmuebles en función de un presupuesto dado. La función recibirá como entrada la lista de inmuebles y un precio, y devolverá otra lista con los inmuebles cuyo precio sea menor o igual que el dado. Los inmuebles de la lista que se devuelva deben incorporar un nuevo par a cada diccionario con el precio del inmueble, donde el precio de un inmueble se calcula con las siguiente fórmula en función de la zona:

- Zona A: precio = (metros * 1000 + habitaciones * 5000 + garaje * 15000) * (1-antiguedad/100)
- Zona B: precio = (metros * 1000 + habitaciones * 5000 + garaje * 15000) * (1-antiguedad/100) * 1.5

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio10.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 11

Escribir una función que reciba una muestra de números y devuelva los valores atípicos, es decir, los valores cuya puntuación típica sea mayor que 3 o menor que -3. 
Nota: La puntuación típica de un valor se obtiene restando la media y dividiendo por la desviación típica de la muestra.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/programacion-funcional/ejercicio11.ipynb" class="btn btn-info">Solución</a>