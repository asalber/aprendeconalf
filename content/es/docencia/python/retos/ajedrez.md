---
title: Ajedrez
summary: Realizar movimientos en un tablero de ajedrez
date: 2019
tags: [Listas, Ficheros]
categories: [Programación, Python]
type: book
---

## Tarea 1

La primera tarea consiste en escribir un programa que guarde en un fichero la secuencia de tableros de una partida de ajedrez. Partiremos del tablero inicial donde las filas del tablero están separadas por cambios de línea y las columnas por tabuladores.

El programa debe guardar el tablero inicial en un fichero con el nombre que elija el usuario. Después debe preguntar al usuario si quiere hacer un movimiento o terminar la partida. Cada vez que el usuario quiera hacer un nuevo movimiento debe preguntar la fila y la columna de la pieza que quiere mover y la fila y la columna a la que la quiere mover. Tras ello añadirá el tablero resultante al final del fichero anterior.

El fichero [partida-ajedrez.txt](doc/partida-ajedrez.txt) contiene un ejemplo con el fichero resultante de una partida con 3 movimientos.

## Tarea 2

Una vez generado el fichero con los tableros sucesivos de una partida de ajedrez, el programa preguntará por un movimiento y mostrará por pantalla el tablero correspondiente ese movimiento.
Por ejemplo, utilizando el fichero [partida-ajedrez.txt](doc/partida-ajedrez.txt), si el usuario introduce el movimiento 2, debería mostrar por pantalla el siguiente tablero:

```sh
♜	♞	♝	♛	♚	♝	♞	♜
♟	♟	♟		♟	♟	♟	♟
							
			♟				
						♙	
							
♙	♙	♙	♙	♙	♙		♙
♖	♘	♗	♕	♔	♗	♘	♖
```

## Solución

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/retos/soluciones/ajedrez.ipynb" class="btn btn-info" target="_blank">Solución</a>
