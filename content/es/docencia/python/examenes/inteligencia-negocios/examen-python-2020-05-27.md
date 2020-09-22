---
title: Examen de Inteligencia de los Negocios 2020-05-27
date: 2020-05-27
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 27 de Mayo de 2020

## Ejercicio 1

Escribir un programa al que al introducirle la altura de una línea sea capaz de dibujarla en diagonal con asteriscos. Por ejemplo, si introducimos `altura = 5` dibujaría lo siguiente:

```python
    *
   *
  *
 *
*
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-05-27/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Escribir una función que cuente las palabras que hay en una frase y las devuelva dentro de un diccionario. También tiene que devolver una lista con las palabras que aparecen más de una vez. Por ejemplo si se le pasa la frase: `La caracola está enterrada al lado de otra caracola de color` la función debe devolver el diccionario y la lista siguientes:

```python
{'La': 1, 'caracola': 2, 'está': 1, 'enterrada': 1, 'al': 1, 'lado': 1, 'de': 2, 'otra': 1, 'color': 1}
['caracola', 'de']
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-05-27/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3
El fichero [horas-trabajo.csv](http://aprendeconalf.es/python/examenes/soluciones/examen-2020-05-27/horas-trabajo.csv) contiene el número de horas mensuales trabajadas por los empleados de una empresa durante el primer cuatrimestre. Crear un programa que realice las siguientes operaciones sin utilizar la librería Pandas:

1. Leer el fichero de internet `http://aprendeconalf.es/python/examenes/soluciones/examen-2020-05-27/horas-trabajo.csv` y crear una lista con las líneas del fichero.
2. Mostrar por pantalla las horas totales del primer operario.
3. Crear un diccionario de diccionarios tal que las claves del diccionario principal serán los identificadores de los operarios y sus valores serán, a su vez, otros diccionarios cuyas claves serán los meses y sus valores las horas trabajadas en esos meses para cada operario. Es decir, un diccionario como el siguiente:

```python
{'OP1': {'Enero': '180', 'Febrero': '160', 'Marzo': '140', 'Abril': '180'},
'OP2': {'Enero': '120', 'Febrero': '140', 'Marzo': '', 'Abril': '100'}, ... }
```

4. Crear una función que reciba la base de datos de las horas trabajadas (puede utilizarse el diccionario del apartado anterior u otra estructura de datos), el identificador de un operario y el precio de la hora, y devuelva una tupla con el número totales de horas trabajadas y el salario de ese operario.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-05-27/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 4

El fichero [horas-trabajo.csv](http://aprendeconalf.es/python/examenes/soluciones/examen-2020-05-27/horas-trabajo.csv) contiene el número de horas mensuales trabajadas por los empleados de una empresa durante el primer cuatrimestre. Crear un programa que realice las siguientes operaciones utilizando la librería Pandas:

1. Crear un DataFrame leyendo el fichero desde internet con la url `http://aprendeconalf.es/python/examenes/soluciones/examen-2020-05-27/horas-trabajo.csv`. Obsérvese que el separador de campos es el punto y coma.
2. Mostrar por pantalla una serie con el número total de horas trabajadas para cada mes.
3. Mostrar por pantalla una serie con el número de operarios de cada departamento.
4. Mostrar por pantalla el número de empleados que han trabajado todos los meses, es decir, que tienen un número de horas todos los meses del cuatrimestre.
5. Convertir el DataFrame a formato largo, de manera que todas las horas aparezcan en la misma columna.
6. Mostrar por pantalla una serie con el número medio de horas trabajadas en cada departamento.
7. Mostrar por pantalla una serie con el total de horas trabajadas de cada operario.
8. Mostrar por pantalla una serie con los salarios de todos los operarios ordenados de mayor a menor.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-05-27/ejercicio4.ipynb" class="btn btn-info" target="_blank">Solución</a>