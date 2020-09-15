---
title: Examen de Inteligencia de los Negocios 2019-05-27
date: 2019-05-27
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 27 de Mayo de 2019

## Ejercicio 1

1. Clonar con git el repositorio con la url `https://github.com/asalberceu/examen-fundamentos-computadores-2019-05-27-parcial1.git`.
2. Crear una rama con los apellidos del alumno en mayúsculas y separados por un guión, es decir, `<APELLIDO1-APELLIDO2>`, y convertir esta rama en la rama activa.
3. Crear el fichero `ejercicio1.3.txt` que contenga la salida del comando de Git que muestra para cada línea del fichero `ejercicio2.py` la información sobre el commit en que se realizó el último cambio en esa línea.
4. Crear un fichero `ejercicio1.4.txt` que contenga la salida del comando que muestra las diferencias entre el primer y el segundo commits del repositorio.
5. Crear un fichero `ejercicio1.5.txt` que contenga la salida del comando de Git que muestra el estado actual del repositorio.
6. Añadir todos los cambios a la zona temporal de intercambio y hacer un commit con el mensaje "Añadidas respuestas."

{{< spoiler text="Solución" >}} 
```sh
> git clone https://github.com/asalberceu/examen-fundamentos-computadores-2019-05-27-parcial1.git
> cd examen-fundamentos-computadores-2019-05-27-parcial1.git
> git checkout -b SANCHEZ-ALBERCA
> git annotate ejercicio2.py > ejercicio1.3.txt
> git diff afce5 b4a76 > ejercicio1.4.txt
> git status > ejercicio1.5.txt
> git add . 
> git commit -m "Añadida respuestas."
```
{{< /spoiler >}}

## Ejercicio 2

Escribir un programa que pida al usuario un número entero $n$ y muestre por pantalla un triángulo el de más abajo.

```
    * 
   ***
  *****
 *******
*********
```

donde $n$ es el número de filas del triángulo.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-05-27/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Escribir un programa para ver los beneficios de una empresa en un periodo de años.

El programa debe cumplir los siguientes requisitos:

- El programa tiene que preguntar al usuario por un año inicial y otro final, y después preguntar por los ingresos y los gastos de cada año desde el año inicial hasta el año final.
- Con los datos introducidos se deben crear dos listas, una con los ingresos y otra con los gastos, de manera que los ingresos y los gastos de cada año aparezcan en la misma posición de las listas.
- El programa debe crear otra lista con el beneficio de cada año (ingresos menos gastos) y mostrarla por pantalla.
- El programa debe crear otra lista booleana que indique para cada año si ha habido beneficios o no y mostrarla por pantalla.
- Finalmente el programa debe mostrar por pantalla la lista de los años con beneficios la lista de los años con pérdidas.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-05-27/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 4

Definir una función que reciba un número entero entre 0 y 999, y devuelva una cadena con la cantidad introducida en palabras. Por ejemplo, si se introduce 647 debe devolver la cadena "seiscientos cuarenta y siete".

La función debe cumplir los siguientes requisitos:

- El único parámetro de entrada de la función es un número entero entre 0 y 999.
- Deben usarse diccionarios para emparejar cada dígito con la palabra correspondiente para las unidades, decenas y centenas.
- Debe devolver una cadena con la cantidad introducida en palabras.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-05-27/ejercicio4.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 5

El fichero [`cotizacion.csv`](cotizacion.csv) contiene las cotizaciones de las empresas del IBEX35 con las siguientes columnas: `nombre` (nombre de la empresa), `Final` (precio de la acción al cierre de bolsa), `Máximo` (precio máximo de la acción durante la jornada), `Mínimo` (precio mínimo de la acción durante la jornada), `volumen` (Volumen al cierre de bolsa), `Efectivo` (capitalización al cierre en miles de euros).

1. Construir una función que abra un fichero con el formato anterior y devuelva un diccionario con los datos del fichero por columnas.

    La función debe cumplir los siguientes requisitos:

    - La función recibirá como único parámetro la ruta del fichero.
    - Debe realizarse un preprocesado de los datos que reemplace la coma por el punto como separador de decimales.
    - Debe realizarse el control de errores mediante excepciones para el caso de que el fichero no exista en la ruta indicada.
    - Debe devolver un diccionario con tantos elementos como columnas tenga el fichero, donde la clave de cada par sea el nombre de la columna y el valor la lista de datos de la columna.

2. Construir una función que reciba el diccionario devuelto por la función anterior y cree un fichero en formato csv con el mínimo, el máximo y la media de dada columna.

    La función debe cumplir los siguientes requisitos:

    - La función recibirá como parámetros el diccionario con los datos de cotización y la ruta del fichero a crear.
    - El fichero generado tendrá las mismas columnas que el fichero `cotizacion.csv` con los mismos nombres de columnas, y tres líneas correspondientes al mínimo, máximo y media de los datos de cada columna. En la columna `nombre` en lugar del nombre de la empresa debe aparecer la medida calculada en esa línea (mínimo, máximo o media). Los datos deben estar separados por punto y coma.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-05-27/ejercicio5.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 6

Definir una función que reciba una lista de facturas, un NIF y un mes, y devuelva un diccionario con el número de facturas emitidas a ese NIF en el mes indicado y el total facturado en ese mes.

La función debe cumplir los siguientes requisitos:

- Los parámetros de entrada serán una lista de facturas, una cadena con un NIF y otra cadena con el mes.
- Cada factura se representarán mediante un diccionario con las claves `nif` (NIF del cliente), `mes` (mes de emisión de la factura), `cantidad` (cantidad facturada sin IVA), `iva` (porcentaje de IVA a aplicar).
- Se debe crear una lista con el total de cada factura (una vez aplicado el IVA) para el NIF y el mes indicados utilizando programación funcional o comprensión de listas.
- La función debe devolver un diccionario con el número de facturas y el total facturado al NIF en el mes indicado.

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/examenes/soluciones/examen-2019-05-27/ejercicio6.ipynb" class="btn btn-info" target="_blank">Solución</a>