---
title: Ejercicios de Depuración
linkTitle: Depuración
date: 
lastmod:
tags: [Ejercicios, Depuración]
categories: [Programación, Python]
type: book
weight: 100
---

## Ejercicio 1

Corregir los errores sintácticos del siguiente programa:

```python
contraseña = input('Introduce la contraseña: ")
if contraseña in ['sesamo'):
  print('Pasa')
else
  print('No pasa')
```

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/depuracion/ejercicio1.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 2

Detectar y corregir los errores del siguiente programa que aplica el iva a una factura:

```python
base = input('Introduce la base imponible de la factura: ')
print(aplica_iva(base, iva))

def aplica_iva(base, iva = 21):
    base = base * iva   
    return base 
```

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/depuracion/ejercicio2.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 3

Detectar y corregir los errores del siguiente programa que calcula el producto escalar de dos vectores:

```python
u = (1, 2, 3)
v = (4, 5, 6)

def producto_escalar(u, v):
    for i in u:
        u[i+1] *= v[i+1]
    return sum(u)

print(producto_escalar(u, v))
```

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/depuracion/ejercicio3.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 4

Detectar y corregir los errores del siguiente programa que devuelve y elimina el teléfono de un listín telefónico a través del nombre del usuario:

```python
listin = {'Juan':123456789, 'Pedro':987654321}

def elimina(listin, usuario):
    del listin[usuario]
    return listin[usuario]

print(elimina(listin, 'Pablo'))
```

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/depuracion/ejercicio4.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 5

Detectar y corregir los errores del siguiente programa que multiplica dos matrices:

```python
a = ((1, 2, 3),
     (3, 2, 1))
b = ((1, 2),
     (3, 4),
     (5, 6))

def producto(a, b):
    producto = []
    for i in range(len(b)):
        fila = []
        for j in range(len(a[0])):
            suma = 0
            for k in range(len(a[0]+1)):
                suma += a[i][k] * b[k+1][j]
            fila[j] = suma
        producto[i] = tuple(fila)
    return tuple(producto)

print(producto(a, b))
```

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/ejercicios/soluciones/depuracion/ejercicio5.ipynb" class="btn btn-info">Solución</a>
