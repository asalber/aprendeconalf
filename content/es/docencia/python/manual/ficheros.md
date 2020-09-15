---
title: Ficheros
lastmod: 
tags: [Ficheros]
categories: [Programación, Python]
type: book
weight: 120
---

## Ficheros

Hasta ahora hemos visto como interactuar con un programa a través del teclado (entrada de datos) y la terminal (salida), pero en la mayor parte de las aplicaciones reales tendremos que leer y escribir datos en ficheros.

Al utilizar ficheros para guardar los datos estos perdurarán tras la ejecución del programa, pudiendo ser consultados o utilizados más tarde.

Las operaciones más habituales con ficheros son:

- Crear un fichero.
- Escribir datos en un fichero.
- Leer datos de un fichero.
- Borrar un fichero.

### Creación y escritura de ficheros

Para crear un fichero nuevo se utiliza la instrucción

`open(ruta, 'w')` : Crea el fichero con la ruta `ruta`, lo abre en modo escritura (el argumento 'w' significa _write_) y devuelve un objeto que lo referencia.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> Si el fichero indicado por la ruta ya existe en el sistema, se reemplazará por el nuevo.

Una vez creado el fichero, para escribir datos en él se utiliza el método

`fichero.write(c)` : Escribe la cadena `c` en el fichero referenciado por `fichero`.

```python
>>> f = open('bienvenida.txt', 'w')
... f.write('¡Bienvenido a Python!')
```

### Añadir datos a un fichero

Si en lugar de crear un fichero nuevo queremos añadir datos a un fichero existente se debe utilizar la instrucción

`open(ruta, 'a')` : Abre el fichero con la ruta `ruta` en modo añadir (el argumento 'a' significa _append_) y devuelve un objeto que lo referencia.

Una vez abierto el fichero, se utiliza el método de escritura anterior y los datos se añaden al final del fichero.

```python
>>> f = open('bienvenida.txt', 'a')
... f.write('\n¡Hasta pronto!')
```

### Leer datos de un fichero

Para abrir un fichero en modo lectura se utiliza la instrucción

`open(ruta, 'r')` : Abre el fichero con la ruta `ruta` en modo lectura (el argumento 'r' significa _read_) y devuelve un objeto que lo referencia.

Una vez abierto el fichero, se puede leer todo el contenido del fichero o se puede leer línea a línea.

### Leer datos de un fichero

`fichero.read()` : Devuelve todos los datos contenidos en `fichero` como una cadena de caracteres.

`fichero.readlines()` : Devuelve una lista de cadenas de caracteres donde cada cadena es una linea del fichero referenciado por `fichero`.

```python
>>> f = open('bienvenida.txt', 'r')
... print(f.read())
¡Bienvenido a Python!
¡Hasta pronto!
```

```python
>>> f = open('bienvenida.txt', 'r')
... lineas = print(f.readlines())
>>> print(lineas)
['Bienvenido a Python!\n', '¡Hasta pronto!']
```

### Cerrar un fichero

Para cerrar un fichero se utiliza el método

`fichero.close()` : Cierra el fichero referenciado por el objeto `fichero`.

Cuando se termina de trabajar con un fichero conviene cerrarlo, sobre todo si se abre en modo escritura, ya que mientras está abierto en este modo no se puede abrir por otra aplicación. Si no se cierra explícitamente un fichero, Python intentará cerrarlo cuando estime que ya no se va a usar más.

```python
>>> f = open('bienvenida.txt'):
... print(f.read())
... f.close()  # Cierre del fichero
...
¡Bienvenido a Python!
¡Hasta pronto!
```

### Renombrado y borrado de un fichero

Para renombra o borrar un fichero se utilizan funciones del módulo `os`.

`os.rename(ruta1, ruta2)` : Renombra y mueve el fichero de la ruta `ruta1` a la ruta `ruta2`.

`os.remove(ruta)` : Borra el fichero de la ruta `ruta`.

Antes de borrar o renombra un directorio conviene comprobar que existe para que no se produzca un error. Para ello se utiliza la función

`os.path.isfile(ruta)` : Devuelve `True` si existe un fichero en la ruta `ruta` y `False` en caso contrario.

### Renombrado y borrado de un fichero o directorio

```python
>>> import os
>>> f = 'bienvenida.txt'
>>> if os.path.isfile(f):
...     os.rename(f, 'saludo.txt') # renombrado
... else:
...     print('¡El fichero', f, 'no existe!')
...
>>> f = 'saludo.txt'
>>> if os.path.isfile(f):
...     os.remove(f) # borrado
... else:
...     print('¡El fichero', f, 'no existe!')
...
```

### Creación, cambio y eliminación de directorios

Para trabajar con directorios también se utilizan funciones del módulo `os`.

`os.listdir(ruta)` : Devuelve una lista con los ficheros y directiorios contenidos en la ruta `ruta`.

`os.mkdir(ruta)` : Crea un nuevo directorio en la ruta `ruta`.

`os.chdir(ruta)` : Cambia el directorio actual al indicado por la ruta `ruta`.

`os.getcwd()` : Devuelve una cadena con la ruta del directorio actual.

`os.rmdir(ruta)` : Borra el directorio de la ruta `ruta`, siempre y cuando esté vacío.

### Leer un fichero de internet

Para leer un fichero de internet hay que utilizar la función `urlopen` del módulo `urllib.request`.

`urlopen(url)` : Abre el fichero con la `url` especificada y devuelve un objeto del tipo fichero al que se puede acceder con los métodos de lectura de ficheros anteriores.

```python
>>> from urllib import request
>>> f = request.urlopen('https://raw.githubusercontent.com/asalber/asalber.github.io/master/README.md')
>>> datos = f.read()
>>> print(datos.decode('utf-8'))
Aprende con Alf
===============

Este es el repositorio del sitio web Aprende con Alf: http://aprendeconalf.es
```
