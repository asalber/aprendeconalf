---
title: Examen de Inteligencia de los Negocios 2021-06-05
date: 2021-06-05
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 5 de junio de 2021

## Ejercicio 1

A veces, al tratar con tuplas, podemos tener un problema en el que necesitamos extraer solo $k$ elementos extremos, es decir, los $k$ máximos y mínimos. Este problema puede tener aplicaciones en campos como el desarrollo web y la ciencia de datos. Desarrollar un programa que dada una tupla y un número $k$ devuelva otra tupla con los $k$ elementos máximos y mínimos.

Ejemplo:

```sh
La tupla original es: (5, 20, 3, 7, 6, 8) 
La tupla con los k = 2 máximos y mínimos es: (3, 5, 8, 20) 
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-06-05/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Construir un programa que evalúe operaciones aritméticas sencillas (sumas, restas, productos, cocientes y potencias) introducidas por el usuario. El programa preguntará por la operación a realizar y el usuario tecleará por pantalla la operación con el siguiente formato:

`operando1 operador operando2`

Después el programa debe mostrar por pantalla el resultado de la operación con el siguiente formato:

`operando1 operador operando2 = resultado`

El programa debe preguntar al usuario hasta que este introduzca la palabra “salir”. También mostrará un mensaje de error si el usuario introduce un número de valores distinto de 3 y si introduce un operador no válido.

Ejemplo:

```sh
Introduce la operación con el formato operando1 operador operando2: 2+3 
Entrada no válida. Debes introducir exactamente tres valores separados por espacio. 
Introduce la operación con el formato operando1 operador operando2: 2 + 3 
2 + 3 = 5.0 
Introduce la operación con el formato operando1 operador operando2: 4 ^ 2 
Operación no válida. 
Introduce la operación con el formato operando1 operador operando2: 4 ** 2 
4 ** 2 = 16.0 
Introduce la operación con el formato operando1 operador operando2: salir 
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-06-05/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

El siguiente diccionario contiene pares formados por números de teléfonos y propietarios:

`{'919654665':'Pedro', '917489210': 'Luis', '623543213':'Carmen', '674833721':'Luis'}`

Crear un programa que construya un diccionario con la misma información, pero tomando como claves los nombres de los usuarios y como valores los teléfonos. Como un usuario puede tener dos teléfonos, uno móvil y uno fijo, los teléfonos deben agruparse a su vez en un diccionario cuyos elementos tendrán clave “movil” o “fijo” según el teléfono empiece por 6 o no. Por ejemplo, a partir del diccionario anterior debe construirse el siguiente diccionario:

`{'Pedro': {'fijo': '919654665'}, 'Luis': {'fijo': '917489210', 'movil': '674833721'}, 'Carmen': {'movil': '623543213'}}`

Después el programa debe recorrer este diccionario y mostrar por pantalla los teléfonos del listín en orden alfabético.

Ejemplo:  

```sh
Teléfonos de Carmen 
         movil : 623543213 
Teléfonos de Luis 
         fijo : 917489210 
         movil : 674833721 
Teléfonos de Pedro 
         fijo : 919654665 
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-06-05/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 4

Construir un programa para realizar las siguientes operaciones con dos números proporcionados por el usuario:

- Comprobar si uno de los dos números es divisible por el otro. Un número es divisible por otro cuando el resto de la división entera es cero.
- Calcular su Máximo Común Divisor.
- Calcular su Mínimo Común Múltiplo.

Cada una de las operaciones deben estar separadas en funciones que tengan como parámetros los 2 números y devuelvan el resultado adecuado.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-06-05/ejercicio4.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 5

El fichero [`cercanias.csv`](../soluciones/examen-2021-06-05/cercanias.csv) contiene información sobre las líneas de tren de cercanías de Madrid: id (identificador del tren), línea (nombre de la línea), estaciones (estaciones de origen y destino separadas por un guion). Se pide:
  
1. Construir una función que lea el fichero `cercanias.csv` y cree un diccionario donde la clave de cada par sea el identificador de la línea y el valor asociado una lista de dos elementos con la estación de origen y la estación de destino como el que se muestra a continuación a modo de ejemplo: 

  `{'10T0001C1': ['Principe Pio', 'Aeropuerto'], '10T0002C1': ['Aeropuerto', 'Principe Pio'], ...}`

  La función debe recibir el nombre del fichero como parámetro.
2. Construir otra función que guarde la información del diccionario obtenido en el apartado anterior en un fichero csv separado por punto y coma con 3 columnas con los encabezados id, origen y destino. La función debe recibir como parámetros el diccionario con los trenes y el nombre del fichero resultante.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-06-05/ejercicio5.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 6

Construir un programa que realize las siguientes operaciones con la librería Pandas:

1. Crear un DataFrame con las siguientes columnas:

    - Nombre: Juan, Marta, Pedro, Jorge, Blas, Lisa, Antonio
    - Edad: 23,78,22,19,45,33,20
    - Género: M, F, M, M, M, F, M
    - Provincia': Burgos, Madrid, Toledo, Burgos, Madrid, Toledo, Madrid
    - Hijos: 2,0,0,3,2,1,4
    - Mascotas: 5,1,0,5,2,2,3

2. Mostrar la información básica del DataFrame.
3. Obtener los principales estadísticos de las columnas numéricas.
4. Obtener los porcentajes de hombres y mujeres por provincias.
5. Representar, mediante un diagrama de dispersión, en número de hijos frente al número de mascotas para las personas de Madrid.
6. Realizar la siguiente gráfica.
!['Recta de regresión'](../img/diagrama-barras-provincias.png)

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-06-05/ejercicio6.ipynb" class="btn btn-info" target="_blank">Solución</a>