---
title: Examen de Inteligencia de los Negocios 2020-06-19
date: 2020-06-19
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 19 de Junio de 2020

## Ejercicio 1

Escribe un programa en python que permita guardar las notas de un alumno conseguidas en un cuatrimestre. Guarda la información en un diccionario cuyas claves sean las asignaturas y los valores las notas de cada asignatura. El programa pedirá la asignatura y la nota para esa asignatura. Si se recibe un número negativo en la nota, el programa termina y muestra las asignaturas suspensas.

Ejemplo

```ssh
Introduce una asignatura: matemáticas
Introduce la nota: 4
Introduce una asignatura: economía
Introduce la nota: 8
Introduce una asignatura: programación
Introduce la nota: 10
Introduce una asignatura: ninguna
Introduce la nota: -2
Las asignaturas suspensas son:
matemáticas
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-06-19/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Escribir una función que tome una lista de números enteros desordenados y devuelva dos listas ordenadas. La primera con los números pares y la segunda con los números impares.


```python
{'La': 1, 'caracola': 2, 'está': 1, 'enterrada': 1, 'al': 1, 'lado': 1, 'de': 2, 'otra': 1, 'color': 1}
['caracola', 'de']
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-06-19/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Escribir un programa para gestionar las citas de una consulta médica. La base de datos de citas debe estar en un fichero de nombre `citas.csv`. Cada cita contendrá los campos `dni`, `mes`, `dia`, `hora` y `especialidad`. No es necesario que la primera fila del csv contenga los nombres de los campos. El programa debe incluir las siguientes funciones:

1. Una función que permita generar el fichero y añadir una cita a la base de datos. 
2. Una función que reciba un dni y devuelva una lista con las citas de ese paciente.
3. Una función para eliminar las citas anteriores a una fecha dada.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-06-19/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 4

El fichero [ipc-2020.csv](http://aprendeconalf.es/python/examenes/soluciones/examen-2020-06-19/ipc-2020.csv) contiene el IPC de las comunidades autónomas de los cinco primeros meses de 2020. Crear un programa que realice las siguientes operaciones utilizando la librería Pandas:

1. Crear un DataFrame leyendo el fichero desde internet con la url `http://aprendeconalf.es/python/examenes/soluciones/examen-2020-06-19/ipc-2020.csv`.
2. Mostrar por pantalla el DataFrame con los datos de las filas 10 a 15.
3. Mostrar por pantalla el DataFrame con los datos de Canarias de Mayo.
4. Mostrar por pantalla una serie con el IPC mensual máximo de cada comunidad autónoma.
5. Mostrar por pantalla una serie con la desviación típica del IPC mensual de cada grupo.
6. Mostrar por pantalla un DataFrame con las comunidades y grupos donde los precios no han subido en promedio (IPC mensual medio menor de 100).

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2020-06-19/ejercicio4.ipynb" class="btn btn-info" target="_blank">Solución</a>