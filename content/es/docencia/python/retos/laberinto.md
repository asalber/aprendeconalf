---
title: Laberinto
summary: Buscar la salida de un laberinto.
date: 2019
tags: [Listas, Bucles]
categories: [Programación, Python]
type: book
---

## Tarea 1
La primera tarea consiste en construir un laberinto como el de la siguiente figura.

![Laberinto](img/laberinto.png)

El laberinto se representará como una una lista de listas, donde cada lista es una fila del laberinto y cada casilla se representará con un espacio ' ' si hay paso o con la letra 'X' si hay un muro, tal y como se muestra a continuación:

```Python
laberinto = [
    [' ', 'X', 'X', 'X', 'X'], 
    [' ', 'X', ' ', ' ', ' '],
    [' ', 'X', ' ', 'X', ' '], 
    [' ', ' ', ' ', 'X', ' '], 
    ['X', 'X', 'X', 'X', 'S']
    ]
```

El laberinto se debe crear a partir de una tupla con las coordenadas de las casillas donde hay muro, como la siguiente:

```Python
muro = ((0,1), (0,2), (0,3), (0,4), (1,1), (2,1), (2,3), (3,3), (4,0), (4,1), (4,2), (4,3))
```

## Tarea 2

La segunda tarea a resolver consiste en construir un programa para recorrer el laberinto desde la entrada a la salida. La entrada siempre está en la esquina superior izquierda y la salida en la esquina inferior derecha.

El programa debe devolver una lista con la secuencia de movimientos para ir de la entrada a la salida del laberinto, tal y como se muestra a continuación:

```Python
['Abajo', 'Abajo', 'Abajo', 'Abajo', 'Derecha', 'Derecha', 'Arriba', 'Arriba', 'Derecha', 'Derecha', 'Abajo', 'Abajo', 'Abajo']
```

## Solución

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/retos/soluciones/laberinto.ipynb" class="btn btn-info" target="_blank">Solución</a>
