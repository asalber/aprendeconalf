---
title: Examen de Inteligencia de los Negocios 2022-03-24
date: 2022-03-24
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 24 de marzo de 2022

## Ejercicio 1

Escriba un programa que permita practicar una variante simplificada de la prueba de cálculo mental _La calculadora humana_ del concurso televisivo Saber y ganar. El usuario debe ir sumando todos los números de la lista de uno en uno hasta que se equivoque o termine la lista, en cuyo caso ganará.

Ejemplo usando la lista [50, 4, 28, 33, 12]: 

```sh
SUMAR Y GANAR 
Vaya sumando todos los números que le iré diciendo. Empezamos por 0. 
Más 50: 50 
Más 4: 54 
Más 28: 72 
Te has equivocado, pero has acertado 2 veces seguidas.


SUMAR Y GANAR 
Vaya sumando todos los números que le iré diciendo. Empezamos por 0. 
Más 50: 50 
Más 4: 54 
Más 28: 82
Más 33: 115
Más 12: 127
Enhorabuena, GANASTE.
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-03-24/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Escribir un programa que calcule a partir de una fecha de un año no bisiesto el número de días que han transcurrido en ese año y el número de meses lunares completos que abarcan. Se recuerda que un mes lunar dura aproximadamente 29,53 días. 

El programa debe usar diccionarios para acceder al número de días de cada mes.

Ejemplo:

```sh
CALENDARIO LUNAR 
Este programa convierte una fecha de un año NO bisiesto a un calendario lunar. 
Indique el día: 1 
Indique el mes: henero 
El mes henero no existe. 

CALENDARIO LUNAR 
Este programa convierte una fecha de un año NO bisiesto a un calendario lunar 
Indique el día: -5 
Indique el mes: marzo 
El día -5 de marzo no existe.

CALENDARIO LUNAR 
Este programa convierte una fecha de un año NO bisiesto a un calendario lunar 
Indique el día: 29 
Indique el mes: febrero 
El día 29 de febrero no existe. 

CALENDARIO LUNAR 
Este programa convierte una fecha de un año NO bisiesto a un calendario lunar 
Indique el día: 1 
Indique el mes: febrero 
El día 1 de febrero es el día 32 del año. 
Habrán pasado 1.08 meses lunares.
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-03-24/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Un cine tiene una sala rectangular con 5 filas y 4 columnas de butacas.  Escribir un programa que permita gestionar la reserva de butacas con los siguientes requisitos:

- El programa mostrará una matriz con el carácter X para las butacas libres y O para las ocupadas y preguntará por la fila y columna de la butaca a reservar.  
- Si el usuario introduce una fila o una columna no válidas, se le avisará y se le volverá a preguntar.  
- Si la fila y la columna introducida corresponde a una butaca ocupada, se avisará al usuario y se le volverá a preguntar.  
- Si la butaca está libre se reservará y se volverá a preguntar al usuario si quiere hacer más reservas.  
- El programa terminará cuando el usuario no quiera hacer más reservas.

Ejemplo:  

```sh
RESERVA DE BUCATAS 
XXXXX  
XXXXX  
XXXXX  
XXXXX  
Introduce la fila que quieres: 2  
Introduce la columna que quieres: 3  
Reserva realizada.  
¿Desea realizar otra reserva? (S/N): S

RESERVA DE BUCATAS 
XXXXX  
XXOXX  
XXXXX  
XXXXX  
Introduce la fila que quieres: 5  
Introduce la columna que quieres: 1  
La fila y columna elegidas no son válidas.  
¿Desea realizar otra reserva? (S/N): S

RESERVA DE BUCATAS  
XXXXX  
XXOXX  
XXXXX  
XXXXX  
Introduce la fila que quieres: 2  
Introduce la columna que quieres: 3  
La butaca elegida está ocupada.  
¿Desea realizar otra reserva? 
(S/N): S

RESERVA DE BUCATAS  
XXXXX  
XXOXX  
XXXXX  
XXXXX  
Introduce la fila que quieres: 1  
Introduce la columna que quieres: 2  
Reserva realizada.  
¿Desea realizar otra reserva? (S/N): N  
¡Gracias! 
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-03-24/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>
