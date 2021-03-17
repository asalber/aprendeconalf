---
title: Bucles
lastmod: 
tags: [Bucles]
categories: [Programación, Python]
type: book
weight: 50
---

## Bucles condicionales (`while`)

> `while` _`condición`_`:`  
&ensp;&ensp;&ensp;&ensp;_`bloque código`_ 

Repite la ejecución del bloque de código mientras la expresión lógica `condición` sea cierta.

Se puede interrumpir en cualquier momento la ejecución del bloque de código con la instrucción `break`.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El bloque de código debe estar indentado por 4 espacios._

```python
>>> # Pregunta al usuario por un número hasta que introduce 0.
>>> num = None
>>> while num != 0:
...     num = int(input('Introduce un número: '))
... 
Introduce un número: 2
Introduce un número: 1
Introduce un número: 0
>>> 
```

Alternativa:

```python
>>> # Pregunta al usuario por un número hasta que introduce 0.
>>> while True:
...     num = int(input('Introduce un número: '))
...     if num == 0:
...         break
...
Introduce un número: 2
Introduce un número: 1
Introduce un número: 0
>>>
```

## Bucles iterativos (`for`)

> `for` _`i`_ `in` _`secuencia`_`:`   
&ensp;&ensp;&ensp;&ensp;_`bloque código`_  

Repite la ejecución del bloque de código para cada elemento de la secuencia `secuencia`, asignado dicho elemento a `i` en cada repetición.

Se puede interrumpir en cualquier momento la ejecución del bloque de código con la instrucción `break` o saltar la ejecución para un determinado elemento de la secuencia con la instrucción `continue`.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El bloque de código debe estar indentado por 4 espacios._

Se utiliza fundamentalmente para recorrer colecciones de objetos como cadenas, listas, tuplas o diccionarios.

A menudo se usan con la instrucción `range`:

- `range(fin)` : Genera una secuencia de números enteros desde 0 hasta `fin-1`.
- `range(inicio, fin, salto)` : Genera una secuencia de números enteros desde `inicio` hasta `fin-1` con un incremento de `salto`.

```python
>>> palabra = 'Python'
>>> for letra in palabra:
...     print(letra)
... 
P
y
t
h
o
n
```

```python
>>> for i in range(1, 10, 2):
...     print(i, end=", ")
...
1, 3, 5, 7, 9, >>>
```
