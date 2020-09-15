---
title: Módulos
lastmod: 
tags: [Módulos]
categories: [Programación, Python]
type: book
weight: 140
---

## Módulos

El código de un programa en Python puede reutilizarse en otro importándolo. Cualquier fichero con código de Python reutilizable se conoce como _módulo_ o _librería_.

Los módulos suelen contener funciones reutilizables, pero también pueden definir variables con datos simples o compuestos (listas, diccionarios, etc), o cualquier otro código válido en Python.

Python permite importar un módulo completo o sólo algunas partes de él. Cuando se importa un módulo completo, el intérprete de Python ejecuta todo el código que contiene el módulo, mientras que si solo se importan algunas partes del módulo, solo se ejecutarán esas partes.

### Importación completa de módulos (`import`)

- `import M` : Ejecuta el código que contiene `M` y crea una referencia a él, de manera que pueden invocarse un objeto o función `f` definida en él mediante la sintaxis `M.f`.

- `import M as N` : Ejecuta el código que contiene `M` y crea una referencia a él con el nombre `N`, de manera que pueden invocarse un objeto o función `f` definida en él mediante la sintaxis `N.f`. Esta forma es similar a la anterior, pero se suele usar cuando el nombre del módulo es muy largo para utilizar un alias más corto.

### Importación parcial de módulos (`from import`)

- `from M import f, g, ...` : Ejecuta el código que contiene `M` y crea referencias a los objetos `f, g, ...`, de manera que pueden ser invocados por su nombre. De esta manera para invocar cualquiera de estos objetos no hace falta precederlos por el nombre del módulo, basta con escribir su nombre.

- `from M import *` : Ejecuta el código que contiene `M` y crea referencias a todos los objetos públicos (aquellos que no empiezan por el carácter `_`) definidos en el módulo, de manera que pueden ser invocados por su nombre.

<i class="fa fa-exclamation-triangle" style="color:red;"></i>Cuando se importen módulos de esta manera hay que tener cuidado de que no haya coincidencias en los nombres de funciones, variables u otros objetos.

```python
>>> import calendar
>>> print(calendar.month(2019, 4))
April 2019
Mo Tu We Th Fr Sa Su
 1  2  3  4  5  6  7
 8  9 10 11 12 13 14
15 16 17 18 19 20 21
22 23 24 25 26 27 28
29 30
```

```python
>>> from math import *
>>> cos(pi)
-1.0
```

### Módulos de la librería estándar más importantes

Python viene con una [biblioteca de módulos predefinidos](https://docs.python.org/3/py-modindex.html) que no necesitan instalarse. Algunos de los más utilizados son:

- [sys](https://docs.python.org/3/library/sys.html): Funciones y parámetros específicos del sistema operativo.
- [os](https://docs.python.org/3/library/os.html): Interfaz con el sistema operativo.
- [os.path](https://docs.python.org/3/library/os.path.html): Funciones de acceso a las rutas del sistema.
- [io](https://docs.python.org/3/library/io.html): Funciones para manejo de flujos de datos y ficheros.
- [string](https://docs.python.org/3/library/string.html): Funciones con cadenas de caracteres.
- [datetime](https://docs.python.org/3/library/datetime.html): Funciones para fechas y tiempos.
- [math](https://docs.python.org/3/library/math.html): Funciones y constantes matemáticas.
- [statistics](https://docs.python.org/3/library/statistics.html): Funciones estadísticas.
- [random](https://docs.python.org/3/library/random.html): Generación de números pseudo-aleatorios.

### Otras librerías imprescindibles

Estas librerías no vienen en la distribución estándar de Python y necesitan instalarse. También puede optarse por la distribución [Anaconda](https://www.anaconda.com/) que incorpora la mayoría de estas librerías.

- [NumPy](https://www.numpy.org/): Funciones matemáticas avanzadas y arrays.
- [SciPy](https://www.scipy.org/): Más funciones matemáticas para aplicaciones científicas.
- [matplotlib](https://matplotlib.org/): Análisis y representación gráfica de datos.
- [Pandas](https://pandas.pydata.org/): Funciones para el manejo y análisis de estructuras de datos.
- [Request](http://www.python-requests.org/en/master/): Acceso a internet por http.