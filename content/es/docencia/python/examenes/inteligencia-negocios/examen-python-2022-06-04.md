---
title: Examen de Inteligencia de los Negocios 2022-06-04
date: 2022-06-06
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 4 de junio de 2022

## Ejercicio 1

Realizar un programa que pregunte al usuario por un número entero impar y dibuje un rombo con el número de filas introducidas por el usuario.

**Ejemplo de ejecución**

```sh
Introduce el número de filas del rombo (un número impar): 7
   *
  ***
 *****
*******
 *****
  ***
   *
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-04-24/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Realizar un programa que simule la operativa de una cuenta bancaria. El programa debe preguntar al usuario si desea realizar un ingreso o un reintegro hasta que el usuario decida terminar el programa.

Si el usuario selecciona la opción de ingreso, debe preguntarle por la cantidad a ingresar e incrementar el saldo en esa cantidad.

Si el usuario selecciona la opción de reintegro deberá preguntarle por la cantidad a sacar y sustraerla del saldo, siempre y cuando haya saldo suficiente. Si no hubiese saldo suficiente avisará al usuario y no realizará el reintegro.

Las cantidades de las operaciones deben guardarse en una sola lista (positivos para ingresos y negativos para reintegros), y después de cada operación debe mostrarse el saldo por pantalla.

Cuando el usuario ya no quiera hacer más operaciones, a partir de la lista de operaciones se deben crear dos listas más, una para los ingresos y otra para los reintegros y deben mostrarse por pantalla.

**Ejemplo de ejecución**

```sh
OPERATIVA CUENTA BANCARIA

¿Qué deseas hacer?
1- Ingreso
2- Reintegro
Elige una opción (cualquier otra para terminar): 1
Introduce la cantidad: 1000
Saldo:  1000.0

¿Qué deseas hacer?
1- Ingreso
2- Reintegro
Elige una opción (cualquier otra para terminar): 2
Introduce la cantidad: 1200
Lo siento, no hay saldo suficiente.

¿Qué deseas hacer?
1- Ingreso
2- Reintegro
Elige una opción (cualquier otra para terminar): 2
Introduce la cantidad: 800
Saldo:  200.0

¿Qué deseas hacer?
1- Ingreso
2- Reintegro
Elige una opción (cualquier otra para terminar): 1
Introduce la cantidad: 500
Saldo:  700.0

¿Qué deseas hacer?
1- Ingreso
2- Reintegro
Elige una opción (cualquier otra para terminar): 2
Introduce la cantidad: 400
Saldo:  300.0

¿Qué deseas hacer?
1- Ingreso
2- Reintegro
Elige una opción (cualquier otra para terminar): 3

Ingresos:  [1000.0, 500.0]
Reintegros: [-800.0, -400.0]
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-04-04/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Existe un texto que se usa frecuentemente para demostraciones dentro del ámbito del diseño gráfico. De hecho, este texto cuyo nombre es Lorem ipsum es un estándar utilizado desde el año 1500 y sirve principalmente para probar el diseño visual antes de insertar el texto definitivo. Dicho pasaje es el siguiente:

_"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."_

Realizar un programa que analice dicho pasaje y realice las siguientes operaciones:

1. Crear un diccionario con la frecuencia de cada carácter sin tener en cuenta el espacio.
2. Muestre por pantalla el caracer que más se repite.
3. Muestre por pantalla las palabras que contienen el caracter más repetido y su frecuencia por palabra.

**Ejemplo de ejecución**

```sh
Carácter más repetido: i
Las palabras donde se encuentra el carácter que más se repite:
{'ipsum': 1, 'sit': 1, 'adipiscing': 3, 'elit,': 1, 'eiusmod': 1, 'incididunt': 3, 'aliqua.': 1, 'enim': 1, 'minim': 2, 'veniam,': 1, 'quis': 1, 'exercitation': 2, 'laboris': 1, 'nisi': 2, 'aliquip': 2, 'Duis': 1, 'irure': 1, 'in': 1, 'reprehenderit': 1, 'velit': 1, 'cillum': 1, 'fugiat': 1, 'pariatur.': 1, 'sint': 1, 'cupidatat': 1, 'proident,': 1, 'qui': 1, 'officia': 2, 'mollit': 1, 'anim': 1, 'id': 1}
```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-04-04/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 4

Escriba un programa que obtenga el máximo y el mínimo de una serie de datos proporcionados en Hexadecimal. Para ello se le pasará una lista de datos en formato hexadecimal, y tendrá que convertirlos primero a formato Binario, y a continuación a formato Decimal. Para ello, se pide lo siguiente:

1. Crear una función de conversión de formato hexadecimal a binario en base a la siguiente tabla:

    | Hexadecimal |  0   |  1   |  2   |  3   |  4   |  5   |  6   |  7   |
    | :---------- | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
    | Decimal     | 0000 | 0001 | 0010 | 0011 | 0100 | 0101 | 0110 | 0111 |
   
    | Hexadecimal |  8   |  9   |  A   |  B   |  C   |  D   |  E   |  F   |
    | :---------- | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
    | Decimal     | 1000 | 1001 | 1010 | 1011 | 1100 | 1101 | 1110 | 1111 |

    **Ejemplo de ejecución**

    ```sh
    Introduce un número hexadecimal: AA55
    El número hexadecimal AA55 en binario es 1010101001010101
    ```

2. Crear una función de conversión de formato binario a decimal. El procedimiento se detalla a continuación:

    ![Conversión de binario a decimal](../img/conversion-binario-decimal.png)

    **Ejemplo de ejecución**
    ```sh
    Introduce un número binario: 1010101001010101
    El número binario 1010101001010101 es en decimal 43605
    ```

3. Crear una función que reciba una lista de números hexadecimales y devuelva una tupla con el máximo y su valor decimal.

    **Ejemplo de ejecución**

    Usando como entrada de la última función la lista: `["AA55", "1010", "BEBE", "0101", "0FEA"]`
    ```sh
    Máximo: ('BEBE', 48830)
    ```

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-04-04/ejercicio4.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 5

El fichero [coches.csv ](https://aprendeconalf.es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-04/coches.csv) contiene información sobre los modelos de coches vendidos en USA un determinado año. Se pide: 

1. Crear un DataFrame a partir del fichero anterior. 
2. Eliminar las filas con valores desconocidos y mostrar el número de filas del dataframe resultante. 
3. Crear una columna con el precio en euros (cambio 1$ = 0.94€) 
4. Mostrar por pantalla las 10 últimas filas del DataFrame. 
5. Mostrar por pantalla el número de marcas que contiene el DataFrame. 
6. Mostrar por pantalla el número de modelos de cada marca que hay en el DataFrame, de mayor a menor frecuencia. 
7. Mostrar por pantalla la marca y el modelo del coche más caro. 
8. Mostrar por pantalla el precio medio en euros de los coches agrupando por marca y ordenando de menor a mayor precio. 
9. Dibujar el diagrama de barras del porcentaje de modelos de cada marca. 
10. Dibujar el diagrama de dispersión de la potencia y el precio.  
Los gráficos deben guardarse en una carpeta con el nombre gráficos y deben tener un título adecuado. 

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-04-04/ejercicio5.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 6

El fichero [bitcoin-tweets.csv](https://aprendeconalf.es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2022-06-04/bitcoin-tweets.csv) contiene los tweets obtenidos en una búsqueda en Twitter sobre bitcoins (cada línea contiene información de un tweet). Se pide: 

1. Crear una función que reciba la url de un fichero csv como el anterior y devuelva una lista con los tweets del fichero, donde cada tweet se represente con un diccionario con sus campos, tal y como se muestra en la siguiente salida: 

    ```sh
    [{'fecha': '2022-05-20 15:11:03+00:00', 'usuario': 'infobaeeconomia', 'texto': 'Bill Gates contra el Bitcoin: “No aporta nada” https://t.co/pZBlC664gw', 'likes': '496'}, 
    {'fecha': '2022-05-21 14:26:51+00:00', 'usuario': 'DaniaGonzalz', 'texto': 'El Salvador hoy es un referente en materia de Inclusión Financiera gracias a la Ley #Bitcoin, países de la región c… https://t.co/P8oS2nfm36', 'likes': '554'}, 
    {'fecha': '2022-05-20 20:42:04+00:00', 'usuario': 'LaHuellaSV', 'texto': 'El asesor en criptoeconomía y fundador de Criptokuántica, Néstor Kreimer, afirmó que El Salvador tiene actualmente… https://t.co/HbSqrQYk67', 'likes': '57'}, 
    {'fecha': '2022-05-20 11:38:19+00:00', 'usuario': 'carmenaidalazo', 'texto': 'La ironía con bitcoin es que años de bajas tasas y politica monetaria expansiva alimentaron incrementos en precios… https://t.co/cm2mo86eKy', 'likes': '284'}, 
    {'fecha': '2022-05-20 11:56:30+00:00', 'usuario': 'garciabanchs', 'texto': 'Cuando a soberbios del #Bitcoin aún les cambiaban los pañales, ya me quemaba las pestañas en mi doctorado de Econom… https://t.co/82tj5Dcalp', 'likes': '74'}, 
    {'fecha': '2022-05-21 14:27:07+00:00', 'usuario': 'DaniaGonzalz', 'texto': '"El Salvador es la capital del #Bitcoin #Ethereum , invitamos a todos los países a invertir en el futuro, por eso nuestro p… https://t.co/UnQVQZj7aw"', 'likes': '89'}, 
    {'fecha': '2022-05-14 00:07:00+00:00', 'usuario': 'ActualidadRT', 'texto': "@ActualidadRT's account has been withheld in Belgium, Austria, Bulgaria, Sweden, Croatia, Spain, Slovenia, Cyprus, Slovakia, Czech Republic, Romania, Portugal, Poland, Denmark, Netherlands, Estonia, Malta, Luxembourg, Finland, France, Lithuania, Germany, Greece, Latvia, Hungary, Italy, Ireland, United Kingdom in response to a legal demand. Learn more.", 'likes': '1037'}, 
    {'fecha': '2022-05-14 14:01:45+00:00', 'usuario': 'ChiguireBipolar', 'texto': 'Testigo de Jehová se esconde de promotor del Bitcoin https://t.co/odVOELmYKu https://t.co/GOtuWLoGhT', 'likes': '1082'}, {'fecha': '2022-05-15 01:21:58+00:00', 'usuario': 'el_pais', 'texto': 'El Salvador convirtió al Bitcoin en su moneda legal. Con la caída de las criptomonedas, han caído en picado también… https://t.co/fFlk1P1LSj', 'likes': '551'}, 
    {'fecha': '2022-05-13 23:00:28+00:00', 'usuario': 'garciabanchs', 'texto': 'La cantidad de dinero que han perdido fans por hacerle caso a celebridades en torno a la adquisición de criptomoned… https://t.co/UOjmvj4Jxq', 'likes': '1143'}, {'fecha': '2022-05-14 15:44:24+00:00', 'usuario': 'juanrallo', 'texto': 'Llevas diciendo que Bitcoin es una burbuja desde que cotizaba a 100 dólares. Que sepamos los patrones típicos de un… https://t.co/2inCgvPHnE', 'likes': '1423'}, {'fecha': '2022-05-14 16:01:48+00:00', 'usuario': 'wallstwolverine', 'texto': 'Los mismos políticos que asesoraban a Venezuela en sus políticas económicas te dan lecciones hoy de lo peligroso qu… https://t.co/wRje03EydN', 'likes': '1543'}, 
    {'fecha': '2022-05-18 06:18:46+00:00', 'usuario': 'EdgardoMulatoSV', 'texto': 'Ya se preguntaron, ¿Por qué sube la ola de homicidios y ataques al Gobierno cuando vienen INVERSIONISTAS al país?… https://t.co/T5PCT8RgKB', 'likes': '796'}]
    ```

2. Crear una función que reciba una lista de tweets como la que devuelve la función anterior, y devuelva un diccionario con los hashtags contenidos en los tweets y su frecuencia, tal y como se muestra en la siguiente salida:

    ```sh
    {'#Bitcoin': 3, '#Ethereum': 1}
    ```


