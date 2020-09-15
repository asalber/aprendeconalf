---
title: Examen de Inteligencia de los Negocios 2019-06-18
date: 2019-06-18
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 18 de Junio de 2019

## Ejercicio 1

1. Clonar con git el repositorio con la url `https://github.com/asalberceu/examen-fundamentos-computadores-2019-06-18-parcial1.git`.
2. Crear una rama con los apellidos del alumno en mayúsculas y separados por un guión, es decir, `<APELLIDO1-APELLIDO2>`, y convertir esta rama en la rama activa.
3. Crear el fichero `ejercicio1.3.txt` que contenga la salida del comando de Git que muestra el historial de commits del repositorio, mostrando un commit por línea.
4. Crear un fichero `ejercicio1.4.txt` que contenga la salida del comando que muestra las diferencias entre el primer y el tercer commits del repositorio.
5. Crear un fichero `ejercicio1.5.txt` que contenga la salida del comando de Git que muestra los repositorios remotos configurados junto con sus urls.
6. Añadir todos los cambios a la zona temporal de intercambio y hacer un commit con el mensaje "Añadidas respuestas ejercicio 1."

{{< spoiler text="Solución" >}}
```sh
> git clone https://github.com/asalberceu/examen-fundamentos-computadores-2019-06-18-parcial1.git
> cd examen-fundamentos-computadores-2019-06-18-parcial1.git
> git checkout -b SANCHEZ-ALBERCA
> git log --oneline > ejercicio1.3.txt
> git diff f9ed835 a485ced > ejercicio1.4.txt
> git remote -v > ejercicio1.5.txt
> git add . 
> git commit -m "Añadida respuestas."
```
{{< /spoiler >}}

## Ejercicio 2

A lo largo de un curso se realizan dos exámenes parciales. Para aprobar el curso la nota media debe ser mayor o igual que 5 siempre y cuando en ambos parciales se tenga al menos un 4. Escribir un programa que pregunte al usuario la nota de los dos parciales y muestre por pantalla si el alumno ha aprobado el curso o si no, y en caso de no haber aprobado, qué parcial tiene que repetir por tener menos de 4 en él.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-06-18/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Un n-grama es una secuencia de $n$ caracteres consecutivos de una cadena. Por ejemplo, los 3-gramas de la cadena `'Python'` son `'Pyt'`, `'yth'`, `'tho'` y `'hon'`. Escribir un programa que pregunte por una cadena y un número entero positivo $n$ y muestre por pantalla todos los n-gramas de la cadena.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-06-18/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 4

Escribir un programa que elimine de una lista dada todos los elementos repetidos y muestre por pantalla los elementos de la lista sin repeticiones.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-06-18/ejercicio4.ipynb" class="btn btn-info" target="_blank">Solución</a>
## Ejercicio 5
Definir funciones para codificar y decodificar mensajes en código morse.

1. Definir una función para codificar una palabra en código morse. Debe cumplir los siguientes requisitos:

   - Debe usarse el diccionario que se da.
   - El único parámetro de entrada de la función es una cadena con una palabra.
   - Debe devolver una cadena con el código morse correspondiente a la palabra, separando los bloques de código correspondientes a cada letra por punto y coma `;`.

2. Definir una función para decodificar una palabra en código morse. Debe cumplir los siguientes requisitos:

   - A partir del diccionario que se da se debe crear el diccionario invertido, es decir, un diccionario cuyas claves son los códigos morse y sus valores las letras correspondientes. Se valorará especialmente el uso de comprensión de diccionarios.
   - El único parámetro de entrada de la función es una cadena de código morse, donde los bloques de código correspondientes a cada letra van separados por puntos y coma `;`.
   - Debe devolver una cadena con la palabra decodificada.

3. Definir una función para codificar un mensaje en código morse. Debe cumplir los siguientes requisitos:

   - Debe usarse la función anterior para codificar palabras.
   - El único parámetro de entrada de la función es una cadena con un mensaje (palabras separadas con espacios).
   - Debe devolver una cadena con las palabras del mensaje codificadas y separadas por espacios.
   - Se valorará especialmente el uso de programación funcional.

4. Definir una función para decodificar un mensaje en código morse. Debe cumplir los siguientes requisitos:

   - Debe usarse la función anterior para decodificar palabras.
   - El único parámetro de entrada de la función es una cadena con un mensaje en código morse (letras separadas por punto y coma, y palabras separadas con espacios).
   - Debe devolver una cadena con las palabras del mensaje decodificadas y separadas por espacios.
   - Se valorará especialmente el uso de programación funcional.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-06-18/ejercicio5.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 6

La url [`https://datos.madrid.es/egob/catalogo/300117-0-arrendamiento-programas.csv`](https://datos.madrid.es/egob/catalogo/300117-0-arrendamiento-programas.csv) apunta a un fichero en formato csv con datos de los arrendamientos de viviendas de la Empresa Municipal de la Vivienda del Ayuntamiento de Madrid. 

1. Construir una función que abra un fichero con el formato anterior y devuelva una lista cuyos elementos son a su vez las listas que contienen los datos de cada línea del fichero menos la primera línea. Debe cumplir los siguientes requisitos:

   - La función recibirá como único parámetro la url del fichero.
   - Debe leer el fichero por líneas y para cada línea debe dividir la línea por el separador de campos (punto y coma) y guardar los datos en una lista.
   - Debe devolver la lista con las listas de datos obtenidas a partir de cada línea.

2. Construir una función que reciba una lista de listas como la que devuelve la función anterior y devuelva otra lista con los nombres de los distritos contenidos en la lista. Debe cumplir los siguientes requisitos:

    - La función recibirá como único parámetro una lista de listas con las viviendas arrendadas por distrito.
    - Debe recorrer la lista de listas y para cada lista debe extraer el nombre del distrito y añadirlo a una lista con los distritos.
    - Debe devolver la lista de distritos.

3. Construir una función que reciba una lista de listas como la que devuelve la primera función y una lista de nombres de distritos y devuelva la lista con las listas correspondientes a los distritos indicados. Debe satisfacer los siguientes requisitos:

    - La función recibirá como parámetros una lista de listas con las viviendas arrendadas por distrito y otra lista con nombres de distritos.
    - Debe recorrer la lista de viviendas arrendadas y añadir a otra lista nueva las líneas correspondientes a los distritos indicados en la segunda lista.
    - Debe devolver la nueva lista con las listas correspondientes a los distritos indicados.

4. Construir una función que reciba una lista como la que devuelve la primera función y devuelva un diccionario cuyas claves sean los nombres de distrito y cuyos valores sean el total de viviendas arrendadas en el distrito. Debe cumplir los siguientes requisitos:

    - La función recibirá como único parámetro la lista con las viviendas arrendadas por distrito.
    - Debe recorrer la lista de listas y para cada lista extraer el nombre del distrito y el total de viviendas arrendadas en el distrito y añadir el par a un diccionario.
    - Debe devolver un diccionario con un par para cada lista de la lista, cuya clave sea el nombre del distrito y cuyo valor sea el número total de viviendas arrendadas en ese distrito.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-06-18/ejercicio6.ipynb" class="btn btn-info" target="_blank">Solución</a>