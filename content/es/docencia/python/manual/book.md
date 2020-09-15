# Python

## ¿Qué es Python?

[Python](https://www.python.org/) es un lenguaje de programación de alto nivel multiparadigma que permite:

- Programación imperativa
- Programación funcional
- Programación orientada a objetos

Fue creado por Guido van Rossum en 1990 aunque actualmente es desarrollado y mantenido por la [Python Software Foundation](https://www.python.org/psf-landing/)

## Principales ventajas de Python

- Es de código abierto (certificado por la OSI).
- Es interpretable y compilable.
- Es fácil de aprender gracias a que su sintaxis es bastante legible para los humanos.
- Es un lenguaje maduro (29 años).
- Es fácilmente extensible e integrable en otros lenguajes (C, java).
- Esta mantenido por una gran comunidad de desarrolladores y hay multitud de recursos para su aprendizaje.

## Tipos de ejecución

### Interpretado en la consola de Python

Se ejecuta cada instrucción que introduce el usuario de manera interactiva.

```sh
> python
>>> name = "Alf"
>>> print("Hola ", name)
Hola Alf
```

### Interpretado en fichero

Se leen y se ejecutan una a una todas las instrucciones del fichero.

```python
# Fichero hola.py
name = "Alf"
print("Hola ", name)
```

```sh
> python hola.py
Hola Alf
```

También se puede hacer el fichero ejecutable indicando en la primera línea la ruta hasta el intérprete de Python.

```{python}
#!/usr/bin/python3
name = "Alf"
print("Hola", name)
```

```sh
> chmod +x hola.py
> ./hola.py
Hola Alf
```

### Compilado a bytecode

```python
# Fichero hola.py
name = "Alf"
print("Hola " + name)
```

```sh
> python -O -m py_compile hola.py
> python __pycache__/hola.cpython-37.pyc
Hola Alf
```

### Compilado a ejecutable del sistema

Hay distintos paquetes que permiten compilar a un ejecutable del sistema operativo usado, por ejemplo `pyinstaller`.

```sh
> conda install pyinstaller
> pyinstaller hola.py
> ./dist/hola/hola
Hola Alf
```

## Tipos de datos primitivos simples

- **Números** (numbers): Secuencia de dígitos (pueden incluir el - para negativos y el . para decimales) que representan números.  
**Ejemplo**. 0, -1, 3.1415.
- **Cadenas** (strings): Secuencia de caracteres alfanuméricos que representan texto. Se escriben entre comillas simples o dobles.  
**Ejemplo**. 'Hola', "Adiós".
- **Booleanos** (boolean): Contiene únicamente dos elementos `True` y `False` que representan los valores lógicos verdadero y falso respectivamente.

Estos datos son inmutables, es decir, su valor es constante y no puede cambiar.

## Tipos de datos primitivos compuestos (contenedores)

- **Listas** (lists): Colecciones de objetos que representan secuencias ordenadas de objetos de distintos tipos. Se representan con corchetes y los elementos se separan por comas.  
**Ejemplo**. [1, "dos", [3, 4], True].
- **Tuplas** (tuples). Colecciones de objetos que representan secuencias ordenadas de objetos de distintos tipos. A diferencia de las listas son inmutables, es decir, que no cambian durante la ejecución. Se representan mediante paréntesis y los elementos se separan por comas.  
**Ejemplo**. (1, 'dos', 3)
- **Diccionarios** (dictionaries): Colecciones de objetos con una clave asociada. Se representan con llaves, los pares separados por comas y cada par contiene una clave y un objeto asociado separados por dos puntos.  
**Ejemplo**. {'pi':3.1416, 'e':2.718}.

## Clase de un dato
#### `type()`

La clase a la que pertenece un dato se obtiene con el comando `type()`

```python
>>> type(1)
<class 'int'>
>>> type("Hola")
<class 'str'>
>>> type([1, "dos", [3, 4], True])
<class 'list'>
>>>type({'pi':3.1416, 'e':2.718})
<class 'dict'>
>>>type((1, 'dos', 3))
<class 'tuple'>
```

## Números (clases `int` y `float`)

Secuencia de dígitos (pueden incluir el - para negativos y el . para decimales) que representan números.
Pueden ser enteros (`int`) o reales (`float`).

```python
>>> type(1)
<class 'int'>
>>> type(-2)
<class 'int'>
>>> type(2.3)
<class 'float'>
```

### Operadores aritméticos

- Operadores aritméticos: `+` (suma), `-` (resta), `*` (producto), `/` (cociente), `//` (cociente división entera), `%` (resto división entera), `**` (potencia).

Orden de prioridad de evaluación:

|       |                        |
| :---: | :--------------------: |
|   1   | Funciones predefinidas |
|   2   |       Potencias        |
|   3   | Productos y cocientes  |
|   4   |     Sumas y restas     |
|       |                        |

Se puede saltar el orden de evaluación utilizando paréntesis `( )`.

```python
>>> 2+3
5
>>> 5*-2
-10
>>> 5/2
2.5
>>> 5//2
2
>>> (2+3)**2
25
```

### Operadores lógicos con números

Devuelven un valor lógico o booleano.

- Operadores lógicos: `==` (igual que), `>` (mayor que), `<` (menor que), `>=` (mayor o igual que), `<=` (menor o igual que), `!=` (distinto de).

```python
>>> 3==3
True
>>> 3.1<=3
False
>>> -1!=1
True
```

## Cadenas (clase `str`)

Secuencia de caracteres alfanuméricos que representan texto. Se escriben entre comillas sencillas `'` o dobles `"`.

```python
'Python'
"123"
'True'
# Cadena vacía
''
# Cadena con un espacio en blanco
' '
# Cambio de línea
'\n'
# Tabulador
'\t'
```

### Acceso a los elementos de una cadena

Cada carácter tiene asociado un índice que permite acceder a él.

|     Cadena      |   P   |   y   |   t   |   h   |   o   |   n   |
| :-------------: | :---: | :---: | :---: | :---: | :---: | :---: |
| Índice positivo |   0   |   1   |   2   |   3   |   4   |   5   |
| Índice negativo |  -6   |  -5   |  -4   |  -3   |  -2   |  -1   |

- `c[i]` devuelve el carácter de la cadena `c` con el índice `i`.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El índice del primer carácter de la cadena es 0._

También se pueden utilizar índices negativos para recorrer la cadena del final al principio.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El índice del último carácter de la cadena es -1._

```python
>>> 'Python'[0]
'P'
>>> 'Python'[1]
'y'
>>> 'Python'[-1]
'n'
>>> 'Python'[6]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: string index out of range
```

### Subcadenas

- `c[i:j:k]` : Devuelve la subcadena de `c` desde el carácter con el índice `i` hasta el carácter anterior al índice `j`, tomando caracteres cada `k`.

```python
>>> 'Python'[1:4]
'yth'
>>> 'Python'[1:1]
''
>>> 'Python'[2:]
'thon'
>>> 'Python'[:-2]
'ytho'
>>> 'Python'[:]
'Python'
>>> 'Python'[0:6:2]
'Pto'
```

### Operaciones con cadenas

- `c1 + c2` : Devuelve la cadena resultado de concatenar las cadenas `c1` y `c2`.
- `c * n` : Devuelve la cadena resultado de concatenar `n` copias de la cadena `c`.
- `c1 in c2` : Devuelve `True` si `c1` es una cadena concenida en `c2` y `False` en caso contrario.
- `c1 not in c2` : Devuelve `True` si `c1` es una cadena no concenida en `c2` y `False` en caso contrario.



```python
>>> 'Me gusta ' + 'Python'
'Me gusta Python'
>>> 'Python' * 3
'PythonPythonPython'
>>> 'y' in 'Python'
True
>>> 'tho' in 'Python'
True
>>> 'to' not in 'Python'
True
```

### Operaciones de comparación de cadenas

- `c1 == c2` : Devuelve `True` si la cadena `c1` es igual que la cadena `c2` y `False` en caso contrario.
- `c1 > c2` : Devuelve `True` si la cadena `c1` sucede a la cadena `c2` y `False` en caso contrario.
- `c1 < c2` : Devuelve `True` si la cadena `c1` antecede a la cadena `c2` y `False` en caso contrario.
- `c1 >= c2` : Devuelve `True` si la cadena `c1` sucede o es igual a la cadena `c2` y `False` en caso contrario.
- `c1 <= c2` : Devuelve `True` si la cadena `c1` antecede o es igual a la cadena `c2` y `False` en caso contrario.
- `c1 != c2` : Devuelve `True` si la cadena `c1` es distinta de la cadena `c2` y `False` en caso contrario.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _Utilizan el orden establecido en el [código ASCII](https://www.codigosascii.com/)_.

### Operaciones de comparación de cadenas

```python
>>> 'Python' == 'python'
False
>>> 'Python' < 'python'
True
>>> 'a' > 'Z'
True
>>> 'A' >= 'Z'
False
>>> '' < 'Python'
True
```

### Funciones de cadenas

- `len(c)` : Devuelve el número de caracteres de la cadena `c`.
- `min(c)` : Devuelve el carácter menor de la cadena `c`.
- `max(c)` : Devuelve el carácter mayor de la cadena `c`.
- `c.upper()` : Devuelve la cadena con los mismos caracteres que la cadena `c` pero en mayúsculas.
- `c.lower()` : Devuelve la cadena con los mismos caracteres que la cadena `c` pero en minúsculas.
- `c.title()` : Devuelve la cadena con los mismos caracteres que la cadena `c` con el primer carácter en mayúsculas y el resto en minúsculas.
- `c.split(delimitador)` : Devuelve la lista formada por las subcadenas que resultan de partir la cadena `c` usando como delimitador la cadena `delimitador`.
Si no se especifica el delimitador utiliza por defecto el espacio en blanco.

<!-- TODO: Incluir más funciones de cadenas como replace -->

## Funciones de cadenas

```python
>>> len('Python')
6
>>> min('Python')
'P'
>>> max('Python')
'y'
>>> 'Python'.upper()
'PYTHON'
>>> 'A,B,C'.split(',')
['A', 'B', 'C']
>>> 'I love Python'.split()
['I', 'love', 'Python']
```

## Datos lógicos o booleanos (clase `bool`)

Contiene únicamente dos elementos `True` y `False` que representan los valores lógicos verdadero y falso respectivamente.

`False` tiene asociado el valor 0 y `True` tiene asociado el valor 1.

### Operaciones con valores lógicos

- Operadores lógicos:  `==` (igual que), `>` (mayor), `<` (menor), `>=` (mayor o igual que), `<=` (menor o igual que), `!=` (distinto de).
- `not b` (negación) : Devuelve `True` si el dato booleano `b` es `False` , y `False` en caso contrario.
- `b1 and b2` : Devuelve `True` si los datos booleanos `b1` y `b2` son `True`, y `False` en caso contrario.
- `b1 or b2` : Devuelve `True` si alguno de los datos booleanos `b1` o `b2` son `True`, y `False` en caso contrario.

### Tabla de verdad

|   `x`   |   `y`   | `not x` | `x and y` | `x or y` |
| :-----: | :-----: | :-----: | :-------: | :------: |
| `False` | `False` | `True`  |  `False`  | `False`  |
| `False` | `True`  | `True`  |  `False`  |  `True`  |
| `True`  | `False` | `False` |  `False`  |  `True`  |
| `True`  | `True`  | `False` |  `True`   |  `True`  |


```python
>>> not True
False
>>> False or True
True
>>> True and False
False
>>> True and True
True
```

## Conversión de datos primitivos simples

Las siguientes funciones convierten un dato de un tipo en otro, siempre y cuando la conversión sea posible.

- `int()` convierte a entero.  
**Ejemplo**. `int('12')` <i class="fa fa-arrow-right"></i> `12`  
`int(True)` <i class="fa fa-arrow-right"></i> `1`   
`int('c')` <i class="fa fa-arrow-right"></i> Error
- `float()` convierte a real.  
**Ejemplo**. `float('3.14')` <i class="fa fa-arrow-right"></i> `3.14`  
`float(True)` <i class="fa fa-arrow-right"></i> `1.0`  
`float('III')` <i class="fa fa-arrow-right"></i> Error
- `str()` convierte a cadena.  
**Ejemplo**. `str(3.14)` <i class="fa fa-arrow-right"></i> `'3.14'`  
`str(True)` <i class="fa fa-arrow-right"></i> `'True'`  
- `bool()` convierte a lógico.  
**Ejemplo**. `bool('0')` <i class="fa fa-arrow-right"></i> `False`  
`bool('3.14')` <i class="fa fa-arrow-right"></i> `True`  
`bool('')` <i class="fa fa-arrow-right"></i> `False`   
`bool('Hola')` <i class="fa fa-arrow-right"></i> `True`

## Variables

Una variable es un identificador ligado a algún valor.

Reglas para nombrarlas:

- Comienzan siempre por una letra, seguida de otras letras o números.
- No se pueden utilizarse palabras reservadas del lenguaje.

A diferencia de otros lenguajes no tienen asociado un tipo y no es necesario declararlas antes de usarlas (tipado dinámico).

Para asignar un valor a una variable se utiliza el operador `=` y para borrar una variable se utiliza la instrucción `del`.

```python
lenguaje = 'Python'
x = 3.14
y = 3 + 2
# Asignación múltiple
a1, a2 = 1, 2
# Intercambio de valores
a, b = b, a
# Incremento (equivale a x = x + 2)
x += 2
# Decremento (equivale a x = x - 1)
x -= 1
# Valor no definido
x = None
del x
```

## Entrada por terminal
#### `input`

Para asignar a una variable un valor introducido por el usuario en la consola se utiliza la instrucción

`input(mensaje)` : Muestra la cadena `mensaje` por la terminal y devuelve una cadena con la entrada del usuario.  

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El valor devuelto siempre es una cadena, incluso si el usuario introduce un dato numérico._

```python
>>> language = input('¿Cuál es tu lenguaje favorito? ')
¿Cuál es tu lenguaje favorito? Python
>>> language
'Python'
>>> age = input('¿Cuál es tu edad? ')
¿Cuál es tu edad? 20
>>> age
'20'
```

### Salida por terminal
#### `print()`

Para mostrar un dato por la terminal se utiliza la instrucción

`print(dato1, ..., sep=' ', end='\n', file=sys.stdout`)

donde

- `dato1, ...` son los datos a imprimir y pueden indicarse tantos como se quieran separados por comas.
- `sep` establece el separador entre los datos, que por defecto es un espacio en blanco `' '`.
- `end` indica la cadena final de la impresión, que por defecto es un cambio de línea `\n`.
- `file` indica la dirección del flujo de salida, que por defecto es la salida estándar `sys.stdout`.

### Salida por terminal
#### `print()`

```python
>>> print('Hola')
Hola
>>> name = 'Alf'
>>> print('Hola', name)
Hola Alf
>>> print('El valor de pi es', 3.1415)
El valor de pi es 3.1415
>>> print('Hola', name, sep='')
HolaAlf
>>> print('Hola', name, end='!\n')
Hola Alf!
```

### Cadenas formateadas
#### `%`

El operador `%` se puede usar también para formatear cadenas.

`print(dato1, ..., sep=' ', end='\n', file=sys.stdout`)

donde

- `dato1, ...` son los datos a imprimir y pueden indicarse tantos como se quieran separados por comas.
- `sep` establece el separador entre los datos, que por defecto es un espacio en blanco `' '`.
- `end` indica la cadena final de la impresión, que por defecto es un cambio de línea `\n`.
- `file` indica la dirección del flujo de salida, que por defecto es la salida estándar `sys.stdout`.

## Condicionales
#### `if`

> `if` <code>condición1:  
&ensp;&ensp;&ensp;&ensp;_bloque código_  
`elif` condición2:  
&ensp;&ensp;&ensp;&ensp;_bloque código_  
...  
`else`:  
&ensp;&ensp;&ensp;&ensp;_bloque código_

Evalúa la expresión lógica `condición1` y ejecuta el primer bloque de código si es `True`; si no, evalúa la siguientes condiciones hasta llegar a la primera que es `True` y ejecuta el bloque de código asociado. Si ninguna condición es `True` ejecuta el bloque de código después de `else:`.

Pueden aparecer varios bloques `elif` pero solo uno `else` al final.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _Los bloques de código deben estar indentados por 4 espacios._

### Condicionales

La instrucción condicional permite evaluar el estado del programa y tomar decisiones sobre qué código ejecutar en función del mismo.

```python
>>> edad = 14
>>> if edad <= 18 : 
...     print('Menor')
... elif edad > 65:
...     print('Jubilado')
... else:
...     print('Activo')
...
Menor
>>> age = 20
>>> if edad <= 18 : 
...     print('Menor')
... elif edad > 65:
...     print('Jubilado')
... else:
...     print('Activo')
...
Activo
```

## Bucles condicionales
#### `while`

> `while condición:`  
&ensp;&ensp;&ensp;&ensp;_`bloque código`_  

Repite la ejecución del bloque de código mientras la expresión lógica `condición` sea cierta.

Se puede interrumpir en cualquier momento la ejecución del bloque de código con la instrucción `break`.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El bloque de código debe estar indentado por 4 espacios._

### Bucles condicionales

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

## Bucles iterativos
#### `for`

> `for i in secuencia:`  
&ensp;&ensp;&ensp;&ensp;_`bloque código`_  

Repite la ejecución del bloque de código para cada elemento de la secuencia `secuencia`, asignado dicho elemento a `i` en cada repetición.

Se puede interrumpir en cualquier momento la ejecución del bloque de código con la instrucción `break` o saltar la ejecución para un determinado elemento de la secuencia con la instrucción `continue`.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El bloque de código debe estar indentado por 4 espacios._

Se utiliza fundamentalmente para recorrer colecciones de objetos como cadenas, listas, tuplas o diccionarios.

### Bucles iterativos

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

## Listas

Una **lista** es una secuencias ordenadas de objetos de distintos tipos.

Se construyen poniendo los elementos entre corchetes `[`  `]` separados por comas.

Se caracterizan por:

- Tienen orden.
- Pueden contener elementos de distintos tipos.
- Son mutables, es decir, pueden alterarse durante la ejecución de un programa.

```python
# Lista vacía
type([])
<class 'list'>
# Lista con elementos de distintos tipos
[1, "dos", True]
# Listas anidadas
[1, [2, 3], 4]
```

### Acceso a los elementos de una lista

Se utilizan los mismos operadores de acceso que para cadenas de caracteres.

- `l[i]` devuelve el elemento de la lista `l` con el índice `i`.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> _El índice del primer elemento de la lista es 0._

```python
>>> a = ['P', 'y', 't', 'h', 'o', 'n']
>>> a[0]
'P'
>>> a[5]
'n'
>>> a[6]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>> a[-1]
'n'
```

### Sublistas

- `l[i:j:k]` : Devuelve la sublista desde el elemento de `l` con el índice `i` hasta el elemento anterior al índice `j`, tomando elementos cada `k`.

```python
>>> a = ['P', 'y', 't', 'h', 'o', 'n']
>>> a[1:4]
['y', 't', 'h']
>>> a[1:1]
[]
>>> a[:-3]
['y', 't', 'h']
>>> a[:]
['P', 'y', 't', 'h', 'o', 'n']
>>> a[0:6:2]
['P', 't', 'o']
```

### Operaciones que no modifican una lista

- `len(l)` : Devuelve el número de elementos de la lista `l`.
- `min(l)` : Devuelve el mínimo elemento de la lista `l` siempre que los datos sean comparables.
- `max(l)` : Devuelve el máximo elemento de la lista `l` siempre que los datos sean comparables.
- `sum(l)` : Devuelve la suma de los elementos de la lista `l`, siempre que los datos se puedan sumar.
- `dato in l` : Devuelve `True` si el dato `dato` pertenece a la lista `l` y `False` en caso contrario.
- `l.index(dato)` : Devuelve la posición que ocupa en la lista `l` el primer elemento con valor `dato`.
- `l.count(dato)` : Devuelve el número de veces que el valor `dato` está contenido en la lista `l`.
- `all(l)` : Devuelve `True` si todos los elementos de la lista `l` son `True` y `False` en caso contrario.
- `any(l)` : Devuelve `True` si algún elemento de la lista `l` es `True` y `False` en caso contrario.

### Operaciones que no modifican una lista

```python
>>> a = [1, 2, 2, 3]
>>> len(a)
4
>>> min(a)
1
>>> max(a)
3
>>> sum(a)
8
>>> 3 in a
True
>>> a.index(2)
1
>>> a.count(2)
2
>>> all(a)
True
>>> any([0, False, 3<2])
False
```

### Operaciones que modifican una lista

- `l1 + l2` : Crea una nueva lista concatenan los elementos de la listas `l1` y `l2`.
- `l.append(dato)` : Añade `dato` al final de la lista `l`. 
- `l.extend(sequencia)` : Añade los datos de `sequencia` al final de la lista `l`.
- `l.insert(índice, dato)` : Inserta `dato` en la posición `índice` de la lista `l` y desplaza los elementos una posición a partir de la posición `índice`.
- `l.remove(dato)` : Elimina el primer elemento con valor `dato` en la lista `l` y desplaza los que están por detrás de él una posición hacia delante.
- `l.pop([índice])` : Devuelve el dato en la posición `índice` y lo elimina de la lista `l`, desplazando los elementos por detrás de él una posición hacia delante.
- `l.sort()` : Ordena los elementos de la lista `l` de acuerdo al orden predefinido, siempre que los elementos sean comparables.
- `l.reverse()` : invierte el orden de los elementos de la lista `l`.

### Operaciones que modifican una lista

```python
>>> a = [1, 3]
>>> b = [2 , 4, 6]
>>> a.append(5)
>>> a
[1, 3, 5]
>>> a.remove(3)
>>> a
[1, 5]
>>> a.insert(1, 3)
>>> a
[1, 3, 5]
>>> b.pop()
6
>>> c = a + b
>>> c
[1, 3, 5, 2, 4]
>>> c.sort()
>>> c
[1, 2, 3, 4, 5]
>>> c.reverse()
>>> c
[5, 4, 3, 2, 1]
```

### Copia de listas

Existen dos formas de copiar listas:

- **Copia por referencia** `l1 = l2`: Asocia la la variable `l1` la misma lista que tiene asociada la variable `l2`, es decir, ambas variables apuntan a la misma dirección de memoria. Cualquier cambio que hagamos a través de `l1` o `l2` afectará a la misma lista.
- **Copia por valor** `l1 = list(l2)`: Crea una copia de la lista asociada a `l2` en una dirección de memoria diferente y se la asocia a `l1`. Las variables apuntan a direcciones de memoria diferentes que contienen los mismos datos. Cualquier cambio que hagamos a través de `l1` no afectará a la lista de `l2` y viceversa.

### Copia de listas

```python
>>> a = [1, 2, 3]
>>> # copia por referencia
>>> b = a
>>> b
[1, 2, 3]
>>> b.remove(2)
>>> b
[1, 3]
>>> a
[1, 3]
```

```python
>>> a = [1, 2, 3]
>>> # copia por referencia
>>> b = list(a)
>>> b
[1, 2, 3]
>>> b.remove(2)
>>> b
[1, 3]
>>> a
[1, 2, 3]
```

## Tuplas

Una **tupla** es una secuencias ordenadas de objetos de distintos tipos.

Se construyen poniendo los elementos entre corchetes `(`  `)` separados por comas.

Se caracterizan por:

- Tienen orden.
- Pueden contener elementos de distintos tipos.
- Son inmutables, es decir, no pueden alterarse durante la ejecución de un programa.

Se usan habitualmente para representar colecciones de datos una determinada estructura semántica, como por ejemplo un vector o una matriz.

```python
# Tupla vacía
type(())
<class 'tuple'>
# Tupla con elementos de distintos tipos
(1, "dos", True)
# Vector
(1, 2, 3)
# Matriz
((1, 2, 3), (4, 5, 6))
```

### Operaciones con tuplas

El acceso a los elementos de una tupla se realiza del mismo modo que en las listas.
También se pueden obtener subtuplas de la misma manera que las sublistas.

Las operaciones de listas que no modifican la lista también son aplicables a las tuplas.

```python
>>> a = (1, 2, 3)
>>> a[1]
2
>>> len(a)
3
>>> a.index(3)
2
>>> 0 in a
False
>>> b = ((1, 2, 3), (4, 5, 6))
>>> b[1]
(4, 5, 6)
>>> b[1][2]
6
```

## Diccionarios

Un diccionario es una colección de pares formados por una _clave_ y un _valor_ asociado a la clave.

Se construyen poniendo los pares entre llaves `{ }` separados por comas, y separando la clave del valor con dos puntos `:`.

Se caracterizan por:

- No tienen orden.
- Pueden contener elementos de distintos tipos.
- Son mutables, es decir, pueden alterarse durante la ejecución de un programa.
- Las claves son únicas, es decir, no pueden repetirse en un mismo diccionario, y pueden ser de cualquier tipo de datos inmutable.

```python
# Diccionario vacío
type({})
<class 'dict'>
# Diccionario con elementos de distintos tipos
{'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
# Diccionarios anidados
{'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca'}}
```

### Acceso a los elementos de un diccionario

- `d[clave]` devuelve el valor del diccionario `d` asociado a la clave `clave`. Si en el diccionario no existe esa clave devuelve un error.
- `d.get(clave, valor)` devuelve el valor del diccionario `d` asociado a la clave `clave`. Si en el diccionario no existe esa clave devuelve `valor`, y si no se especifica un valor por defecto devuelve `None`.

```python
>>> a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
>>> a['nombre']
'Alfredo'
>>> a['despacho'] = 210
>>> a
{'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
>>> a.get('email')
'asalber@ceu.es'
>>> a.get('universidad', 'CEU')
'CEU'
```

### Operaciones que no modifican un diccionario

- `len(d)` : Devuelve el número de elementos del diccionario `d`.
- `min(d)` : Devuelve la mínima clave del diccionario `d` siempre que las claves sean comparables.
- `max(d)` : Devuelve la máxima clave del diccionario `d` siempre que las claves sean comparables.
- `sum(d)` : Devuelve la suma de las claves del diccionario `d`, siempre que las claves se puedan sumar.
- `clave in d` : Devuelve `True` si la clave `clave` pertenece al diccionario `d` y `False` en caso contrario.
- `d.keys()` : Devuelve un iterador sobre las claves de un diccionario.
- `d.values()` : Devuelve un iterador sobre los valores de un diccionario.
- `d.items()` : Devuelve un iterador sobre los pares clave-valor de un diccionario.

### Operaciones que no modifican un diccionario

```python
>>> a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
>>> len(a)
3
>>> min(a)
'despacho'
>>> 'email' in a
True
>>> a.keys()
dict_keys(['nombre', 'despacho', 'email'])
>>> a.values()
dict_values(['Alfredo', 218, 'asalber@ceu.es'])
>>> a.items()
dict_items([('nombre', 'Alfredo'), ('despacho', 218), ('email', 'asalber@ceu.es')])
```

### Operaciones que modifican un diccionario

- `d[clave] = valor` : Añade al diccionario `d` el par formado por la clave `clave` y el valor `valor`.
- `d.update(d2)`. Añade los pares del diccionario `d2` al diccionario `d`. 
- `d.pop(clave, alternativo)` : Devuelve del valor asociado a la clave `clave` del diccionario `d` y lo elimina del diccionario. Si la clave no está devuelve el valor `alternativo`.
- `d.popitem()` : Devuelve la tupla formada por la clave y el valor del último par añadido al diccionario `d` y lo elimina del diccionario.
- `del d[clave]` : Elimina del diccionario `d` el par con la clave `clave`.
- `d.clear()` : Elimina todos los pares del diccionario `d` de manera que se queda vacío.

### Operaciones que modifican un diccionario

```python
>>> a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
>>> a['universidad'] = 'CEU'
>>> a
{'nombre': 'Alfredo', 'despacho': 218, 'email': 'asalber@ceu.es', 'universidad': 'CEU'}
>>> a.pop('despacho')
218
>>> a
{'nombre': 'Alfredo', 'email': 'asalber@ceu.es', 'universidad': 'CEU'}
>>> a.popitem()
('universidad', 'CEU')
>>> a
{'nombre': 'Alfredo', 'email': 'asalber@ceu.es'}
>>> del a['email']
>>> a
{'nombre': 'Alfredo'}
>>> a.clear()
>>> a
{}
```

### Copia de diccionarios

Existen dos formas de copiar diccionarios:

- **Copia por referencia** `d1 = d2`: Asocia la la variable `d1` el mismo diccionario que tiene asociado la variable `d2`, es decir, ambas variables apuntan a la misma dirección de memoria. Cualquier cambio que hagamos a través de `l1` o `l2` afectará al mismo diccionario.
- **Copia por valor** `d1 = list(d2)`: Crea una copia del diccionario asociado a `d2` en una dirección de memoria diferente y se la asocia a `d1`. Las variables apuntan a direcciones de memoria diferentes que contienen los mismos datos. Cualquier cambio que hagamos a través de `l1` no afectará al diccionario de `l2` y viceversa.

### Copia de diccionarios

```python
>>> a = {1:'A', 2:'B', 3:'C'}
>>> # copia por referencia
>>> b = a
>>> b
{1:'A', 2:'B', 3:'C'}
>>> b.pop(2)
>>> b
{1:'A', 3:'C'}
>>> a
{1:'A', 3:'C'}
```

```python
>>> a = {1:'A', 2:'B', 3:'C'}
>>> # copia por referencia
>>> b = dict(a)
>>> b
{1:'A', 2:'B', 3:'C'}
>>> b.pop(2)
>>> b
{1:'A', 3:'C'}
>>> a
{1:'A', 2:'B', 3:'C'}
```

## Funciones
#### `def`

Una función es un bloque de código que tiene asociado un nombre, de manera que cada vez que se quiera ejecutar el bloque de código basta con invocar el nombre de la función.

Para declarar una función se utiliza la siguiente sintaxis:

> `def <nombre-funcion> (<parámetros>):`  
&ensp;&ensp;&ensp;&ensp; _`bloque código`_  
&ensp;&ensp;&ensp;&ensp; `return <objeto>`

```python
>>> def bienvenida():
...     print('¡Bienvenido a Python!')
...     return
...
>>> type(bienvenida)
<class 'function'>
>>> bienvenida()
¡Bienvenido a Python!
```

### Parámetros de una función

Una función puede recibir valores cuando se invoca a través de unas variables conocidas como _parámetros_ que se definen entre paréntesis en la declaración de la función. En el cuerpo de la función se pueden usar estos parámetros como si fuesen variables.

Los valores que se pasan a la función en una invocación concreta de ella se conocen como _argumentos_ y se asocian a los parámetros de la declaración de la función.

```python
>>> def bienvenida(nombre):
...     print('¡Bienvenido a Python', nombre + '!')
...     return
...
>>> bienvenida('Alf')
¡Bienvenido a Python Alf!
```

### Argumentos de la llamada a una función

Los valores que se pasan a la función en una llamada o invocación concreta de ella se conocen como _argumentos_ y se asocian a los parámetros de la declaración de la función.

Los argumentos se pueden indicar de dos formas:

- **Argumentos posicionales**: Se asocian a los parámetros de la función en el mismo orden que aparecen en la definición de la función.
- **Argumentos por nombre**: Se indica explícitamente el nombre del parámetro al que se asocia un argumento de la forma `parametro = argumento`.

```python
>>> def bienvenida(nombre, apellido):
...     print('¡Bienvenido a Python', nombre, apellido + '!')
...     return
...
>>> bienvenida('Alfredo', 'Sánchez)
¡Bienvenido a Python Alfredo Sánchez!
>>> bienvenida(apellido = 'Sánchez', nombre = 'Alfredo')
¡Bienvenido a Python Alfredo Sánchez!
```

### Retorno de una función

Una función puede devolver un objeto de cualquier tipo tras su invocación. Para ello el objeto a devolver debe escribirse detrás de la palabra reservada `return`. Si no se indica ningún objeto, la función no devolverá nada.

```python
>>> def area_triangulo(base, altura):
...     return base * altura / 2
...
>>> area_triangulo(2, 3)
3
>>> area_triangulo(4, 5)
10
```

## Argumentos por defecto

En la definición de una función se puede asignar a cada parámetro un argumento por defecto, de manera que si se invoca la función sin proporcionar ningún argumento para ese parámetro, se utiliza el argumento por defecto.

```python
>>> def bienvenida(nombre, lenguaje = 'Python'):
...     print('¡Bienvenido a', lenguaje, nombre + '!')
...     return
...
>>> bienvenida('Alf')
¡Bienvenido a Python Alf!
>>> bienvenida('Alf', 'Java')
¡Bienvenido a Java Alf!
```

## Pasar un número indeterminado de argumentos

Por último, es posible pasar un número variable de argumentos a un parámetro. Esto se puede hacer de dos formas:

- `*parametro`: Se antepone un asterisco al nombre del parámetro y en la invocación de la función se pasa el número variable de argumentos separados por comas. Los argumentos se guardan en una lista que se asocia al parámetro.
- `**parametro`: Se anteponen dos asteriscos al nombre del parámetro y en la invocación de la función se pasa el número variable de argumentos por pares `nombre = valor`, separados por comas. Los argumentos se guardan en un diccionario que se asocia al parámetro.


```python
>>> def menu(*platos):
...     print('Hoy tenemos: ', end='')
...     for plato in platos:
...         print(plato, end=', ')
...     return
...
>>> menu('pasta', 'pizza', 'ensalada')
Hoy tenemos: pasta, pizza, ensalada,
```

## Ámbito de los parámetros y variables de una función
Los parámetros y las variables declaradas dentro de una función son de **ámbito local**, mientras que las definidas fuera de ella son de ámbito **ámbito global**.

Tanto los parámetros como las variables del ámbito local de una función sólo están accesibles durante la ejecución de la función, es decir, cuando termina la ejecución de la función estas variables desaparecen y no son accesibles desde fuera de la función.

```python
>>> def bienvenida(nombre):
...     lenguaje = 'Python'
...     print('¡Bienvenido a', lenguaje, nombre + '!')
...     return
...
>>> bienvenida('Alf')
¡Bienvenido a Python Alf!
>>> lenguaje
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'lenguaje' is not defined
```

## Ámbito de los parámetros y variables de una función
Si en el ámbito local de una función existe una variable que también existe en el ámbito global, durante la ejecución de la función la variable global queda eclipsada por la variable local y no es accesible hasta que finaliza la ejecución de la función.

```python
>>> lenguaje = 'Java'
>>> def bienvenida():
...     lenguaje = 'Python'
...     print('¡Bienvenido a', lenguaje + '!')
...     return
...
>>> bienvenida()
¡Bienvenido a Python!
>>> print(lenguaje)
Java
```

## Paso de argumentos por referencia

En Python el paso de argumentos a una función es siempre por referencia, es decir, se pasa una referencia al objeto del argumento, de manera que cualquier cambio que se haga dentro de la función mediante el parámetro asociado afectará al objeto original, siempre y cuando este sea mutable.

```python
>>> primer_curso = ['Matemáticas', 'Física']
>>> def añade_asignatura(curso, asignatura):
...     curso.append(asignatura)
...     return
...
>>> añade_asignatura(primer_curso, 'Química')
>>> print(primer_curso)
['Matemáticas', 'Física', 'Química']
```

## Documentación de funciones

Una práctica muy recomendable cuando se define una función es describir lo que la función hace en un comentario.

En Python esto se hace con un **docstring** que es un tipo de comentario especial se hace en la línea siguiente al encabezado de la función entre tres comillas simples `'''` o dobles `"""`.

Después se puede acceder a la documentación de la función con la función `help(<nombre-función>)`.

```python
>>> def area_triangulo(base, altura):
... """Función que calcula el área de un triángulo.
...
... Parámetros:
...     - base: La base del triángulo.
...     - altura: La altura del triángulo.
... Resultado:
...     El área del triángulo con la base y altura especificadas.
... """
...     return base * altura / 2
...
>>> help(area_triangulo)
area_triangulo(base, altura)
    Función que calcula el área de un triángulo.

    Parámetros:
        - base: La base del triángulo.
        - altura: La altura del triángulo.
    Resultado:
        El área del triángulo con la base y altura especificadas.
```

## Funciones recursivas

Una función recursiva es una función que en su cuerpo contiene una llama a si misma.

La recursión es una práctica común en la mayoría de los lenguajes de programación ya que permite resolver las tareas recursivas de manera más natural.

Para garantizar el final de una función recursiva, las sucesivas llamadas tienen que reducir el grado de complejidad del problema, hasta que este pueda resolverse directamente sin necesidad de volver a llamar a la función.

```python
>>> def factorial(n):
...     if n == 0:
...         return 1
...     else:
...         return n * factorial(n-1)
...
>>> f(5)
120
```

### Funciones recursivas múltiples

Una función recursiva puede invocarse a si misma tantas veces como quiera en su cuerpo.

```python
>>> def fibonacci(n):
...     if n <= 1:
...         return n
...     else:
...         return fibonacci(n - 1) + fibonacci(n - 2)
...
>>> fibonacci(6)
8
```

### Los riesgos de la recursión

Aunque la recursión permite resolver las tareas recursivas de forma más natural, hay que tener cuidado con ella porque suele consumir bastante memoria, ya que cada llamada a la función crea un nuevo ámbito local con las variables y los parámetros de la función.

En muchos casos es más eficiente resolver la tarea recursiva de forma iterativa usando bucles.

```python
>>> def fibonacci(n):
...     a, b = 0, 1
...     for i in range(n):
...         a, b = b, a + b
...     return a
...
>>> fibonacci(6)
8
```

## Importación de funciones
#### `import`

Las funciones definidas en un programa o módulo de Python pueden ser importadas y reutilizadas en otros programas.

Existen varias formas de importar módulos y funciones:

- `import M` : Importa el módulo `M` y crea una referencia a él, de manera que pueden invocarse un objeto o función `f` definida en él mediante la sintaxis `M.f`.

- `import M as N` : Importa el módulo `M` y crea una referencia `N` a él, de manera que pueden invocarse un objeto o función `f` definida en él mediante la sintaxis `N.f`. Esta forma es similar a la anterior, pero tiene se suele usar cuando el nombre del módulo es muy largo para utilizar un alias más corto.

### Importación de funciones
#### `from import`

- `from M import *` : Importa el módulo `M` y crea referencias a todos los objetos públicos (aquellos que no empiezan por el carácter `_`) definidos en el módulo. De esta manera para invocar un objeto del módulo no hace falta precederlo por el nombre del módulo, basta con escribir su nombre.
  
- `from M import f, g, ...` : Importa el módulo `M` y crea referencias a los objetos `f, g, ...`, de manera que pueden ser invocados por su nombre.

### Importación de funciones

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

No necesitan instalarse porque vienen incluidos en la distribución de Python.

- [sys](https://docs.python.org/3/library/sys.html): Funciones y parámetros específicos del sistema operativo.
- [os](https://docs.python.org/3/library/os.html): Interfaz con el sistema operativo.
- [os.path](https://docs.python.org/3/library/os.path.html): Funciones de acceso a las rutas del sistema.
- [io](https://docs.python.org/3/library/io.html): Funciones para manejo de flujos de datos y ficheros.
- [string](https://docs.python.org/3/library/string.html): Funciones con cadenas de caracteres.
- [datetime](https://docs.python.org/3/library/datetime.html): Funciones para fechas y tiempos.
- [math](https://docs.python.org/3/library/math.html): Funciones y constantes matemáticas.
- [statistics](https://docs.python.org/3/library/statistics.html): Funciones estadísticas.
- [random](https://docs.python.org/3/library/random.html): Generación de números pseudo-aleatorios.

## Otros módulos imprescindibles

Necesitan instalarse.

- [NumPy](https://www.numpy.org/): Funciones matemáticas avanzadas y arrays.
- [SciPy](https://www.scipy.org/): Más funciones matemáticas para aplicaciones científicas.
- [matplotlib](https://matplotlib.org/): Análisis y representación gráfica de datos.
- [Pandas](https://pandas.pydata.org/): Funciones para el manejo y análisis de estructuras de datos.
- [Request](http://www.python-requests.org/en/master/): Acceso a internet por http.

## Programación funcional

En Python las funciones son objetos de primera clase, es decir, que pueden pasarse como argumentos de una función, al igual que el resto de los tipos de datos.

```python
>>> def aplica(funcion, argumento):
...     return funcion(argumento)
...
>>> def cuadrado(n):
...     return n*n
...
>>> def cubo(n):
...     return n**3
...
>>> aplica(cuadrado, 5)
25
>>> aplica(cubo, 5)
125
```

### Funciones anónimas
#### `lambda`

Existe un tipo especial de funciones que no tienen nombre asociado y se conocen como **funciones anónimas** o **funciones lambda**.

La sintaxis para definir una función anónima es

> `lambda <parámetros> : <expresión>`

Estas funciones se suelen asociar a una variable o parámetro desde la que hacer la llamada.

```python
>>> area = lambda base, altura : base * altura
>>> area(4, 5)
10
```

### Aplicar una función a todos los elementos de una colección iterable
#### `map`

`map(f, c)` : Devuelve una objeto iterable con los resultados de aplicar la función `f` a los elementos de la colección `c`. Si la función `f` requiere `n` argumentos entonces deben pasarse `n` colecciones con los argumentos. Para convertir el objeto en una lista, tupla o diccionario hay que aplicar explícitamente las funciones `list()`, `tuple()` o `dic()` respectivamente.

```python
>>> def cuadrado(n):
...     return n * n
...
>>> list(map(cuadrado, [1, 2, 3])
[1, 4, 9]
```
```python
>>> def rectangulo(a, b):
...     return a * b
...
>>> tuple(map(rectangulo, (1, 2, 3), (4, 5, 6)))
(4, 10, 18)
```

### Filtrar los elementos de una colección iterable
#### filter

`filter(f, c)` : Devuelve una objeto iterable con los elementos de la colección `c` que devuelven `True` al aplicarles la función `f`. Para convertir el objeto en una lista, tupla o diccionario hay que aplicar explícitamente las funciones `list()`, `tuple()` o `dic()` respectivamente.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> `f` debe ser una función que recibe un argumento y devuelve un valor booleano.

```python
>>> def par(n):
...     return n % 2 == 0
...
>>> list(filter(par, range(10))
[0, 2, 4, 6, 8]
```

### Combinar los elementos de varias colecciones iterables
#### `zip`

`zip(c1, c2, ...)` : Devuelve un objeto iterable cuyos elementos son tuplas formadas por los elementos que ocupan la misma posición en las colecciones `c1`, `c2`, etc. El número de elementos de las tuplas es el número de colecciones que se pasen. Para convertir el objeto en una lista, tupla o diccionario hay que aplicar explícitamente las funciones `list()`, `tuple()` o `dic()` respectivamente.

```python
>>> asignaturas = ['Matemáticas', 'Física', 'Química', 'Economía']
>>> notas = [6.0, 3.5, 7.5, 8.0]
>>> list(zip(asignaturas, notas))
[('Matemáticas', 6.0), ('Física', 3.5), ('Química', 7.5), ('Economía', 8.0)]
>>> dict(zip(asignaturas, notas[:3]))
{'Matemáticas': 6.0, 'Física': 3.5, 'Química': 7.5}
```

### Operar todos los elementos de una colección iterable
#### `reduce`

`reduce(f, l)` : Aplicar la función `f` a los dos primeros elementos de la secuencia `l`. Con el valor obtenido vuelve a aplicar la función `f` a ese valor y el siguiente de la secuencia, y así hasta que no quedan más elementos en la lista. Devuelve el valor resultado de la última aplicación de la función `f`.

La función `reduce` está definida en el módulo `functools`.

```python
>>> from functools import reduce
>>> def producto(n, m):
...     return n * m
...
>>> reduce(producto, range(1, 5))
24
```

## Comprensión de colecciones

En muchas aplicaciones es habitual aplicar una función o realizar una operación con los elementos de una colección (lista, tupla o diccionario) y obtener una nueva colección de elementos transformados. Aunque esto se puede hacer recorriendo la secuencia con un bucle iterativo, y en programación funcional mediante la función `map`, Python incorpora un mecanismo muy potente que permite esto mismo de manera más simple.

### Comprensión de listas

> [_expresion_ `for` _variable_ `in` _lista_ `if` _condicion_]

Esta instrucción genera la lista cuyos elementos son el resultado de evaluar la expresión _expresion_, para cada valor que toma la variable _variable_, donde _variable_ toma todos los valores de la lista _lista_ que cumplen la condición _condición_.

```python
>>> [x ** 2 for x in range(10)]
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
>>> [x for x in range(10) if x % 2 == 0]
[0, 2, 4, 6, 8]
>>> [x ** 2 for x in range(10) if x % 2 == 0]
[0, 4, 16, 36, 64]
>>> notas = {'Carmen':5, 'Antonio':4, 'Juan':8, 'Mónica':9, 'María': 6, 'Pablo':3}
>>> [nombre for (nombre, nota) in notas.items() if nota >= 5]
['Carmen', 'Juan', 'Mónica', 'María']
```

### Comprensión de diccionarios

> {_expresion-clave_`:`_expresion-valor_ `for` _variables_ `in` _lista_ `if` _condicion_}

Esta instrucción genera el diccionario formado por los pares cuyas claves son el resultado de evaluar la expresión _expresion-clave_ y cuyos valores son el resultado de evaluar la expresión _expresion-valor_, para cada valor que toma la variable _variable_, donde _variable_ toma todos los valores de la lista _lista_ que cumplen la condición _condición_.

```python
>>> {palabra:len(palabra) for palabra in ['I', 'love', 'Python']}
{'I': 1, 'love': 4, 'Python': 6}
>>> notas = {'Carmen':5, 'Antonio':4, 'Juan':8, 'Mónica':9, 'María': 6, 'Pablo':3}
>>> {nombre: nota +1 for (nombre, nota) in notas.items() if nota >= 5])
{'Carmen': 6, 'Juan': 9, 'Mónica': 10, 'María': 7}
```

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

## Control de errores mediante excepciones

Python utiliza un objeto especial llamado **excepción** para controlar cualquier error que pueda ocurrir durante la ejecución de un programa.

Cuando ocurre un error durante la ejecución de un programa, Python crea una excepción. Si no se controla esta excepción la ejecución del programa se detiene y se muestra el error (_traceback_).

```python
>>> print(1 / 0)  # Error al intentar dividir por 0.
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

### Tipos de excepciones

Los principales excepciones definidas en Python son:

- `TypeError` : Ocurre cuando se aplica una operación o función a un dato del tipo inapropiado.
- `ZeroDivisionError` : Ocurre cuando se itenta dividir por cero.
- `OverflowError` : Ocurre cuando un cálculo excede el límite para un tipo de dato numérico.
- `IndexError` : Ocurre cuando se intenta acceder a una secuencia con un índice que no existe.
- `KeyError` : Ocurre cuando se intenta acceder a un diccionario con una clave que no existe.
- `FileNotFoundError` : Ocurre cuando se intenta acceder a un fichero que no existe en la ruta indicada.
- `ImportError` : Ocurre cuando falla la importación de un módulo.

Consultar la documentaciónde Python para ver la [lista de exepciones predefinidas](https://docs.python.org/3/library/exceptions.html).

### Control de excepciones
#### `try - except - else`

Para evitar la interrución de la ejecución del programa cuando se produce un error, es posible controlar la exepción que se genera con la siguiente instrucción:

> `try:`  
&ensp;&ensp;&ensp;&ensp; _bloque código 1_  
`except` _excepción_`:`  
&ensp;&ensp;&ensp;&ensp; _bloque código 2_  
`else:`  
&ensp;&ensp;&ensp;&ensp; _bloque código 3_

Esta instrucción ejecuta el primer bloque de código y si se produce un error que genera una excepción del tipo _excepción_ entonces ejecuta el segundo bloque de código, mientras que si no se produce ningún error, se ejecuta el tercer bloque de código.

### Control de excepciones

```python
>>> def division(a, b):
...     try:
...         result = a / b
...     except ZeroDivisionError:
...         print('¡No se puede dividir por cero!')
...     else:
...         print(result)
...
>>> division(1, 0)
¡No se puede dividir por cero!
>>> division(1, 2)
0.5
```

```python
>>> try:
...     f = open('fichero.txt')  # El fichero no existe
... except FileNotFoundError:
...     print('¡El fichero no existe!')
... else:
...     print(f.read())
¡El fichero no existe!
```

<!-- TODO: Añadir sección de programación orientada a objetos -->

## La librería NumPy

[NumPy](https://www.numpy.org) es una librería de Python especializada en el cálculo numérico y el análisis de datos, especialmente para un gran volumen de datos.

Incorpora una nueva clase de objetos llamados **arrays** que permite representar colecciones de datos de un mismo tipo en varias dimensiones, y funciones muy eficientes para su manipulación.

<img src="img/numpy-logo.png" alt="Gráfico con matplotlib" height="200px">

## La clase de objetos `array`

Un array es una estructura de datos de un mismo tipo organizada en forma de tabla o cuadrícula de distintas dimensiones.

Las dimensiones de un array también se conocen como **ejes**.

<img src="img/arrays.png" alt="Gráfico con matplotlib" height="400px">

## Creación de arrays

Para crear un array se utiliza la siguiente función de NumPy

`np.array(secuencia)` : Crea un array a partir de la lista o tupla `lista` y devuelve una referencia a él. El número de dimensiones del array dependerá de las listas o tuplas anidadas en `lista`:

- Para una lista de valores se crea un array de una dimensión, también conocido como **vector**.
- Para una lista de listas de valores se crea un array de dos dimensiones, también conocido como **matriz**.
- Para una lista de listas de listas de valores se crea un array de tres dimensiones, también conocido como **cubo**.
- Y así sucesivamente. No hay límite en el número de dimensiones del array más allá de la memoria disponible en el sistema.

<i class="fa fa-exclamation-triangle" style="color:red;"></i> Los elementos de la lista o tupla deben ser del mismo tipo.

### Creación de arrays

```python
>>> # Array de una dimensión
>>> a1 = np.array([1, 2, 3])
>>> print(a1)
[1 2 3]
>>> # Array de dos dimensiones
>>> a2 = np.array([[1, 2, 3], [4, 5, 6]])
>>> print(a2)
[[1 2 3]
 [4 5 6]]
>>> # Array de tres dimensiones
>>> a3 = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])
>>> print(a3)
[[[ 1  2  3]
  [ 4  5  6]]

 [[ 7  8  9]
  [10 11 12]]]
```

### Creación de arrays

Otras funciones útiles que permiten generar arrays son:

`np.empty(dimensiones)` : Crea y devuelve una referencia a un array vacío con las dimensiones especificadas en la tupla `dimensiones`.

`np.zeros(dimensiones)` : Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla `dimensiones` cuyos elementos son todos ceros.

`np.ones(dimensiones)` : Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla `dimensiones` cuyos elementos son todos unos.

`np.full(dimensiones, valor)` : Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla `dimensiones` cuyos elementos son todos `valor`.

`np.identity(n)` : Crea y devuelve una referencia a la matriz identidad de dimensión `n`.

`np.arange(inicio, fin, salto)` : Crea y devuelve una referencia a un array de una dimensión cuyos elementos son la secuencia desde `inicio` hasta `fin` tomando valores cada `salto`.

`np.linspace(inicio, fin, n)` : Crea y devuelve una referencia a un array de una dimensión cuyos elementos son la secuencia de `n` valores equidistantes desde `inicio` hasta `fin`.

`np.random.random(dimensiones)` : Crea y devuelve una referencia a un array con las dimensiones especificadas en la tupla `dimensiones` cuyos elementos son aleatorios.

## Creación de arrays

```python
>>> print(np.zeros(3,2))
[[0. 0. 0.]
 [0. 0. 0.]]
>>> print(np.idendity(3))
[[1. 0. 0.]
 [0. 1. 0.]
 [0. 0. 1.]]
>>> print(np.arange(1, 10, 2))
[1 3 5 7 9]
>>> print(np.linspace(0, 10, 5))
[ 0.   2.5  5.   7.5 10. ]
```

### Atributos de un array

Existen varios atributos y funciones que describen las características de un array.

`a.ndi` : Devuelve el número de dimensiones del array `a`.

`a.shape` : Devuelve una tupla con las dimensiones del array `a`.

`a.size` : Devuelve el número de elementos del array `a`.

`a.dtype`: Devuelve el tipo de datos de los elementos del array `a`.

### Acceso a los elementos de un array

Para acceder a los elementos contenidos en un array se usan índices al igual que para acceder a los ementos de una lista, pero indicando los índices de cada dimensión separados por comas.

Al igual que para listas, los índices de cada dimensión comienzn en 0.

También es posible obtener subarrays con el operador dos puntos `:` indicando el índice inicial y el siguiente al final para cada dimensión, de nuevo separados por comas.

```python
>>> a = np.array([[1, 2, 3], [4, 5, 6]])
>>> print(a[1, 0])  # Acceso al elemento de la fila 1 columna 0
4
>>> print(a[1][0])  # Otra forma de acceder al mismo elemento
4
>>> print(a[:, 0:2])
[[1 2]
 [4 5]]
```

### Filtrado de elementos de un array

Una característica muy útil de los arrays es que es muy fácil obtener otro array con los elementos que cumplen una condición.

`a[condicion]` : Devuelve una lista con los elementos del array `a` que cumplen la condición `condicion`.

```python
>>> a = np.array([[1, 2, 3], [4, 5, 6]])
>>> print(a[(a % 2 == 0)])
[2 4 6]
>>> print(a[(a % 2 == 0) &  (a > 2)])
[2 4]
```

### Operaciones matemáticas con arrays

Existen dos formas de realizar operaciones matemáticas con arrays: a nivel de elemento y a nivel de array.

Las operaciones a nivel de elemento operan los elementos que ocupan la misma posición en dos arrays. Se necesitan, por tanto, dos arrays con las mismas dimensiones y el resultado es una array de la misma dimensión.

Los operadores mamemáticos `+`, `-`, `*`, `/`, `%`, `**` se utilizan para la realizar suma, resta, producto, cociente, resto y potencia a nivel de elemento.

```python
>>> a = np.array([[1, 2, 3], [4, 5, 6]])
>>> b = np.array([[1, 1, 1], [2, 2, 2]])
>>> print(a + b )
[[2 3 4]
 [6 7 8]]
>>> print(a / b)
[[1.  2.  3. ]
 [2.  2.5 3. ]]
>>> print(a ** 2)
[[ 1  4  9]
 [16 25 36]]
```

### Operaciones matemáticas a nivel de array

Para realizar el producto matricial se utiliza el método

`a.dot(b)` : Devuelve el array resultado del producto matricial de los arrays `a` y `b` siempre y cuando sus dimensiones sean compatibles.

Y para trasponer una matriz se utiliza el método

`a.T` : Devuelve el array resultado de trasponer el array `a`.

```python
>>> a = np.array([[1, 2, 3], [4, 5, 6]])
>>> b = np.array([[1, 1], [2, 2], [3, 3]])
>>> print(a.dot(b))
[[14 14]
 [32 32]]
>>> print(a.T)
[[1 4]
 [2 5]
 [3 6]]
```

## La librería Pandas

[Pandas](https://pandas.pydata.org) es una librería de Python especializada en el manejo y análisis de estructuras de datos.

Las principales características de esta librería son:

- Define el tipo de objetos`DataFrame` para manejar conjuntos de datos.
- Permite leer y escribir facilmente ficheros en formato CSV, Excel y bases de datos SQL.
- Ofrece métodos para reordenar, dividir y combinar conjuntos de datos.
- Permite trabajar con series temporales.
- Ofrece un rendimiento muy eficiente.

<img src="img/pandas-logo.png" alt="Gráfico con matplotlib" height="150px">

### La clase de objetos DataFrame

Un objeto del tipo `DataFrame` define un conjunto de datos estructurado en forma de tabla donde las columnas suelen contener datos de variables, es decir, todos los datos de una misma columna son del mismo tipo, y las filas de individuos que pueden contender datos de distintos tipos.

| Nombre    | Edad | Grado          | Correo              |
| :-------- | :--- | :------------- | :------------------ |
| 'María'   | 18   | 'Economía'     | 'maria@gmail.com'   |
| 'Luis     | 22   | 'Medicina'     | 'luis@yahoo.es'     |
| 'Carmen'  | 20   | 'Arquitectura' | 'carmen@gmail.com'  |
| 'Antonio' | 21   | 'Economía'     | 'antonio@gmail.com' |

### Creación de un DataFrame a partir de un diccionario

`DataFrame(diccionario)` : Crea un objeto del tipo DataFrame con los datos del diccionario `diccionario`. Las claves del diccionario serán los nombres de las columnas, mientras que los valores asociados a las claves serán listas con los valores de las columnas.

```python
>>> import pandas as pd
>>> datos = {'nombre':['María', 'Luis', 'Carmen', 'Antonio'],
... 'edad':[18, 22, 20, 21],
... 'grado':['Economía', 'Medicina', 'Arquitectura', 'Economía'],
... 'correo':['maria@gmail.com', 'luis@yahoo.es', 'carmen@gmail.com', 'antonio@gmail.com']
... }
>>> df = pd.DataFrame(datos)
>>> print(df)
    nombre  edad         grado             correo
0    María    18      Economía    maria@gmail.com
1     Luis    22      Medicina      luis@yahoo.es
2   Carmen    20  Arquitectura   carmen@gmail.com
3  Antonio    21      Economía  antonio@gmail.com
```

### Importación de ficheros

Dependiendo del tipo de fichero, existen distintas funciones para importar un DataFrame desde un fichero.

`read_csv(fichero.csv, delimitador)` : Devuelve un objeto del tipo DataFrame con los datos del fichero CSV `fichero.csv` usando como separador de los datos la cadena `delimitador`.

`read_excel(fichero.xlsx, hoja)` : Devuelve un objeto del tipo DataFrame con los datos de la hoja de cálculo `hoja` del fichero Excel `fichero.xlx`.

```python
>>> import pandas as pd
>>> # Importación del fichero datos-colesterol.csv
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
>>> print(df.head())
                              nombre  edad sexo  peso  altura  colesterol
0       José Luis Martínez Izquierdo    18    H    85     179         182
1                     Rosa Díaz Díaz    32    M    65     173         232
2              Javier García Sánchez    24    H    71     181         191
3                Carmen López Pinzón    35    M    65     170         200
4               Marisa López Collado    46    M    51     158         148
```

### Exportación de ficheros

También existen funciones para exportar un DataFrame a un fichero con diferentes formatos.

`df.to_csv(fichero.csv, delimitador)` : Exporta el DataFrame `df` al fichero `fichero.csv` en formato CSV usando como separador de los datos la cadena `delimitador`.

`df.to_excel(fichero.xlsx, sheet_name = hoja)` : Exporta el DataFrame `df` a la hoja de cálculo `hoja` del fichero `fichero.xlsx` en formato Excel.

### Atributos de un DataFrame

Existen varias propiedades o métodos para ver las características de un DataFrame.

`df.info()` : Devuelve información (número de filas, número de columnas, nombre y tipo de las columnas y memoria usado) sobre el DataFrame `df`.

`df.shape` : Devuelve una tupla con el número de filas y columnas del DataFrame `df`.

`df.columns` : Devuelve el nombre de las columnas del DataFrame `df`.

`df.head()` : Devuelve las 5 primeras filas del DataFrame `df`.

`df.tails()` : Devuelve las 5 últimas filas del DataFrame `df`.

### Acceso a los elementos de un DataFrame mediante índices

El acceso a los datos de un DataFrame se puede hacer a través de índices o través de los nombres de las filas y columnas.
Para acceder a los elementos de un DataFrame mediante índices se utiliza un método similar al de las listas o arrays.

`df.iloc[i, j]` : Devuelve el elemento que se encuentra en la fila `i` y la columna `j` del DataFrame `df`. Puede indicarse secuencias de índices para obtener partes del DataFrame.

`df.iloc[i]` : Devuelve la fila `i` del DataFrame `df`.

```python
>>> import pandas as pd
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
>>> print(df.iloc[1, 3])
65
>>> print(df.iloc[1, :2])
nombre     Rosa Díaz Díaz
edad                   32
```

### Acceso a los elementos de un DataFrame mediante nombres

`df.loc[fila, columna]` : Devuelve el elemento que se encuentra en la fila de nombre `fila` y la columna de nombre `columna` del DataFrame `df`.

`df[columna]` : Devuelve los elementos de la columna de nombre `columna` del DataFrame `df`.

```python
>>> import pandas as pd
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
>>> print(df.loc[2, 'colesterol']
191
>>> print(df.loc[:3, ('colesterol','peso')])
   colesterol  peso
1         232    65
2         191    71
3         200    65
>>> print(df['colesterol'])
0     182
1     232
2     191
3     200
...
```

### Operaciones sobre columnas

Puesto que los datos de una misma columna de un DataFrame tienen que ser del mismo tipo, es fácil aplicar la misma operación a todos los elementos de la columna.

```python
>>> import pandas as pd
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
>>> print(df['altura']/100)
0     1.79
1     1.73
2     1.81
...

>>> print(df['sexo']=='M')
0     False
1      True
2     False
...

```

### Aplicar funciones a columnas

Para aplicar funciones a todos los elementos de una columna se utiliza el método

`df[columna].apply(f)` : Devuelve una secuencia con los valores que resulta de aplicar la función `f` a los elementos de la columna de nombre  `columna` del DataFrame `df`.

```python
>>> import pandas as pd
>>> from math import log
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
>>> print(df['altura'].apply(log))
0     5.187386
1     5.153292
2     5.198497
...
```

### Filtrado de un DataFrame

Una operación bastante común con un DataFrame es obtener las filas que cumplen una determinada condición.

`df[condicion]` : Devuelve un DataFrame con las filas del DataFrame `df` que se corresponden con el valor `True` de la secuencia booleana `condicion`. `condicion` debe ser una secuencia de valores booleanos de la misma longitud que el número de filas del DataFrame.

```python
>>> import pandas as pd
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
>>> print(df[(df['sexo']=='H') & (df['colesterol'] > 260)])
                     nombre  edad sexo  peso  altura  colesterol
6   Antonio Fernández Ocaña    51    H    62     172         276
9   Santiago Reillo Manzano    46    H    75     185         280
```

## Eliminar filas y columnas de un DataFrame

Para eliminar filas y columnas de un DataFrame se utiliza el método

`df.drop(filas)` : Devuelve el DataFrame que resulta de eliminar las filas con los nombres indicados en la secuencia `filas` del DataFrame `df`.

`df.drop(columnas, axis=1)` : Devuelve el DataFrame que resulta de eliminar las columnas con los nombres indicados en la secuencia `columnas` del DataFrame `df`.

```python
>>> import pandas as pd
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
>>> print(df.drop([1, 3]))
0       José Luis Martínez Izquierdo    18    H    85     179         182
2              Javier García Sánchez    24    H    71     181         191
4               Marisa López Collado    46    M    51     158         148
...
>>> print(df.drop(['peso', 'altura'], axis=1))
0       José Luis Martínez Izquierdo    18    H         182
1                     Rosa Díaz Díaz    32    M         232
2              Javier García Sánchez    24    H         191
...
```

### Ordenar un DataFrame

Para ordenar un DataFrame de acuedo a los valores de una determinada columna se utiliza el método

`df.sort_values(columna)` : Devuelve el DataFrame que resulta de ordenar ascendentemente el DataFrame `df` según los valores del la columna `columna`.

`df.sort_values(columna, ascending=False)` : Devuelve el DataFrame que resulta de ordenar descendentemente el DataFrame `df` según los valores del la columna `columna`.  

```python
>>> import pandas as pd
>>> df = pd.read_csv(
'https://raw.githubusercontent.com/asalber/manual-python/master/datos/colesterol.csv')
print(df.sort_values('colesterol'))
                              nombre  edad sexo  peso  altura  colesterol
4               Marisa López Collado    46    M    51     158         148
0       José Luis Martínez Izquierdo    18    H    85     179         182
2              Javier García Sánchez    24    H    71     181         191
13             Carolina Rubio Moreno    20    M    61     177         194
...
```

### Reestructurar un DataFrame: Convertir columnas en filas

A menudo la disposición de los datos en un DataFrame no es la adecuada para su tratamiento y es necesario reestructurar el DataFrame.

Para convertir columnas en filas se utiliza el método

`df.melt(id_vars, var_name, var_value)`

```python
>>> import pandas as pd
>>> datos = {'nombre':['María', 'Luis', 'Carmen'],
... 'edad':[18, 22, 20],
... 'Matemáticas':[8.5, 7, 3.5],
... 'Física':[8, 6.5, 5],
... 'Química':[6.5, 4, 9]}
>>> df = pd.DataFrame(datos)
>>> df1 = df.melt(id_vars=['nombre', 'edad'], var_name='asignatura', value_name='nota')
>>> print(df1)
   nombre  edad   asignatura  nota
0   María    18  Matemáticas   8.5
1    Luis    22  Matemáticas   7.0
2  Carmen    20  Matemáticas   3.5
3   María    18       Física   8.0
4    Luis    22       Física   6.5
5  Carmen    20       Física   5.0
6   María    18      Química   6.5
7    Luis    22      Química   4.0
8  Carmen    20      Química   9.0
```

### Reestructurar un DataFrame: Convertir filas en columnas

Para convertir columnas en filas se utiliza el método

`df.pivot(index, columns, values)`

```python
# Continuación del código anterior
>>> print(df1.pivot(index='nombre', columns='asignatura', values='nota'))
asignatura  Física  Matemáticas  Química
nombre                                  
Carmen         5.0          3.5      9.0
Luis           6.5          7.0      4.0
María          8.0          8.5      6.5
```

## La librería Matplotlib

[Matplotlib](https://matplotlib.org/) es una librería de Python especializada en la creación de gráficos en dos dimensiones.

<img src="img/matplotlib-logo.png" alt="Gráfico con matplotlib" height="150px">

### Tipos de gráficos

Permite crear y personalizar los tipos de gráficos más comunes, entre ellos:

- Diagramas de barras
- Histograma
- Diagramas de sectores
- Diagramas de caja y bigotes
- Diagramas de violín
- Diagramas de dispersión o puntos
- Diagramas de lineas
- Diagramas de areas
- Diagramas de contorno
- Mapas de color

y combinaciones de todos ellos.

En la siguiente [galería de gráficos](https://matplotlib.org/gallery/index.html) pueden apreciarse todos los tipos de gráficos que pueden crearse con esta librería.

### Creación de gráficos con matplotlib

Para crear un gráfico con matplotlib es habitual seguir los siguientes pasos:


1. Importar el módulo `pyplot`.

2. Definir la figura que contendrá el gráfico, que es la region (ventana o página) donde se dibujará. Para ello se utiliza la función `figure()`.

3. Definir los ejes sobre los que se dibujarán los datos. Para ello se utiliza la función `add_axes()` o bien `add_subplot()`.
  
4. Dibujar los datos sobre los ejes. Para ello se utilizan distintas funciones dependiendo del tipo de gráfico que se quiera.

5. Personalizar el gráfico. Para ello existen multitud de funciones que permiten añadir un título, una leyenda, una rejilla, cambiar colores o personalizar los ejes.

6. Guardar el gráfico. Para ello se utiliza la función `savefig()`.

7. Mostrar el gráfico. Para ello se utiliza la función `show()`.

### Creación de gráficos con matplotlib

```python
# Importar el módulo pyplot con el alias plt
import matplotlib.pyplot as plt
# Crear la figura
fig = plt.figure()
# Crear los ejes
ax = fig.add_subplot(111)
# Dibujar puntos
ax.scatter(x = [1, 2, 3], y = [3, 2, 1])
# Guardar el gráfico en formato png
plt.savefig('diagrama-dispersion.png')
# Mostrar el gráfico
plt.show()
```

<img src="img/diagrama-dispersion.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de dispersión o puntos

- `scatter(x, y)`: Dibuja un diagrama de puntos con las coordenadas de la lista `x` en el eje X y las coordenadas de la lista `y` en el eje Y. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.scatter.html#matplotlib.pyplot.scatter)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.scatter([1, 2, 3, 4], [1, 2, 0, 0.5])
plt.show()
```

<img src="img/diagrama-puntos.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de líneas

- `plot(x, y)`: Dibuja un polígono con los vértices dados por las coordenadas de la lista `x` en el eje X y las coordenadas de la lista `y` en el eje Y. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.plot.html#matplotlib.pyplot.plot)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.plot([1, 2, 3, 4], [1, 2, 0, 0.5])
plt.show()
```

<img src="img/diagrama-lineas.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de areas

- `fill_between(x, y)`: Dibuja el area bajo el polígono con los vértices dados por las coordenadas de la lista `x` en el eje X y las coordenadas de la lista `y` en el eje Y. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.fill_between.html#matplotlib.pyplot.fill_between)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.fill_between([1, 2, 3, 4], [1, 2, 0, 0.5])
plt.show()
```

<img src="img/diagrama-areas.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de barras verticales

- `bar(x, y)`: Dibuja un diagrama de barras verticales donde `x` es una lista con la posición de las barras en el eje X, e `y` es una lista con la altura de las barras en el eje Y. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.bar.html#matplotlib.pyplot.bar)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.bar([1, 2, 3], [3, 2, 1])
plt.show()
```

<img src="img/diagrama-barras.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de barras horizontales

- `barh(x, y)`: Dibuja un diagrama de barras horizontales donde `x` es una lista con la posición de las barras en el eje Y, y `x` es una lista con la longitud de las barras en el eje X. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.barh.html#matplotlib.pyplot.barh)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.barh([1, 2, 3], [3, 2, 1])
plt.show()
```

<img src="img/diagrama-barras-horizontales.png" alt="Gráfico con matplotlib" height="300px">

### Histogramas

- `hist(x, bins)`: Dibuja un histograma con las frecuencias resultantes de agrupar los datos de la lista `x` en las clases definidas por la lista `bins`. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.hist.html#matplotlib.pyplot.hist)

```python
import numpy as np
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
x = np.random.normal(5, 1.5, size=1000)
ax.hist(x, np.arange(0, 11))
plt.savefig('histograma.png')
plt.show()
```

<img src="img/histograma.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de sectores

- `pie(x)`: Dibuja un diagrama de sectores con las frecuencias de la lista `x`. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.pie.html#matplotlib.pyplot.pie)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.pie([5, 4, 3, 2, 1]
plt.savefig('diagrama-sectores.png')
plt.show()
```

<img src="img/diagrama-sectores.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de caja y bigotes

- `boxplot(x)`: Dibuja un diagrama de caja y bigotes con los datos de la lista `x`. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.boxplot.html#matplotlib.pyplot.boxplot)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.boxplot([1, 2, 1, 2, 3, 4, 3, 3, 5, 7])
plt.savefig('diagrama-sectores.png')
plt.show()
```

<img src="img/diagrama-caja.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de violín

- `violinplot(x)`: Dibuja un diagrama de violín con los datos de la lista `x`. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.violinplot.html#matplotlib.pyplot.violinplot)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
ax.violinplot([1, 2, 1, 2, 3, 4, 3, 3, 5, 7])
plt.savefig('diagrama-sectores.png')
plt.show()
```

<img src="img/diagrama-violin.png" alt="Gráfico con matplotlib" height="300px">

### Diagramas de contorno

- `contourf(x, y, z)`: Dibuja un diagrama de contorno con las curvas de nivel de la superficie dada por los puntos con las coordenadas de las listas `x`, `y` y `z` en los ejes X, Y y Z respectivamente. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.contourf.html#matplotlib.pyplot.contourf)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
x = np.linspace(-3.0, 3.0, 100)
y = np.linspace(-3.0, 3.0, 100)
x, y = np.meshgrid(x, y)
z = np.sqrt(x**2 + 2*y**2)
ax.contourf(x, y, z)
plt.show()
```

<img src="img/diagrama-contorno.png" alt="Gráfico con matplotlib" height="300px">

### Mapas de color

- `imshow(x)`: Dibuja un mapa de color a partir de una matriz (array bidimensiona) `x`. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.imshow.html#matplotlib.pyplot.imshow)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
x = np.random.random((16, 16))
ax.imshow(x)
plt.show()
```

<img src="img/mapa-calor.png" alt="Gráfico con matplotlib" height="300px"> <i class="fa fa-info-circle" aria-hidden="true">

### Mapas de color

- `hist2d(x, y)`: Dibuja un mapa de color que simula un histograma bidimensional, donde los colores de los cuadrados dependen de las frecuencias de las clases de la muestra dada por las listas `x` e `y`. [<i class="fa fa-info-circle" aria-hidden="true"></i>](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.hist2d.html#matplotlib.pyplot.hist2d)

```python
import matplotlib.pyplot as plt
fig = plt.figure()
ax = fig.add_subplot(111)
x, y = np.random.multivariate_normal(mean=[0.0, 0.0], cov=[[1.0, 0.4], [0.4, 0.5]], size=1000).T
ax.hist2d(x, y)
plt.show()
```

<img src="img/histograma2D.png" alt="Gráfico con matplotlib" height="300px">

### Colores

### Líneas

### Títulos

### Ejes

### Leyenda

### Regilla

### Texto

### Márgenes

## Referencias

Webs:

- [Python](https://www.python.org/) Sitio web de Python.
- [Repl.it](https://repl.it/) Entorno de desarrollo web para varios lenguajes, incluido Python.
- [Python tutor](http://pythontutor.com/) Sitio web que permite visualizar la ejecución el código Python.

## Referencias

Libros y manuales:

- [Tutorial de Python](https://www.tutorialpython.com/) Tutorial rápido de python.
- [Python para todos](http://mundogeek.net/tutorial-python/) Libro de introducción a Python con muchos ejemplos. Es de licencia libre.
- [Python para principiantes](https://www.safecreative.org/work/1207302042960-curso-python-para-principiantes) Libro de introducción Python que abarca orientación a objetos. Es de licencia libre.
- [Python crash course](https://ehmatthes.github.io/pcc/) Libro de introducción a Python gratuito.
- [Think python 2e](http://greenteapress.com/wp/think-python-2e/). Libro de introducción a Python que abarca también algoritmos, estructuras de datos y gráficos. Es de licencia libre.
- [Learning Python](http://shop.oreilly.com/product/0636920028154.do) Libro de introducción a Python con enfoque de programación orientada a objetos.

## Referencias

Vídeos:

- [Curso "Python para todos"](https://www.edx.org/course/programming-for-everybody-getting-started-with-python).