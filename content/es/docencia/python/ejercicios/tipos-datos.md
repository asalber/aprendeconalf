---
title: Ejercicios de Tipos de Datos Simples
linkTitle: Tipos de Datos Simples
date: 
lastmod:
tags: [Ejercicios, Tipos de Datos]
categories: [Programación, Python]
type: book
weight: 10
---

<!-- Datacamp light
<script async type="text/javascript" src="https://cdn.datacamp.com/dcl-react-dev.js.gz"></script>  
-->

## Ejercicio 1

Escribir un programa que muestre por pantalla la cadena `¡Hola Mundo!`.

<!-- <div><button class="resolution">Resolver</button></div>
<div data-datacamp-exercise data-lang="python" id="solution" style="display: none">

  <code data-type="sample-code">
    # Mostrar por pantalla la cadena "¡Hola mundo!"

  </code>

  <code data-type="solution">
  # Mostrar por pantalla la cadena "¡Hola mundo!"
  print("¡Hola mundo!")
  </code>
  
  <code data-type="sct">

  Ex().multi(
    check_function("print"),
    has_output("¡Hola mundo!", pattern = False)
  )
  success_msg("¡Correcto!")
  </code>
  
  <div data-type="hint">
    Usa la función <code>print</code> para mostrar cadenas por pantalla.
  </div>
</div> -->

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio1.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 2

Escribir un programa que almacene la cadena `¡Hola Mundo!` en una variable y luego muestre por pantalla el contenido de la variable.

<!-- <div><button class="resolution">Resolver</button></div>
<div data-datacamp-exercise data-lang="python" id="solution" style="display: none">

  <code data-type="sample-code">
    # Guardar la cadena "¡Hola mundo!" en la variable a

    # Mostrar por pantalla contenido de la variable a

  </code>

  <code data-type="solution">
    # Guardar la cadena "¡Hola mundo!" en la variable a
    a = "¡Hola mundo!"

    # Mostrar por pantalla contenido de la variable a  
    print(a)
    </code>
  
  <code data-type="sct">
    Ex().multi(
      check_object("a").has_equal_value(),
      check_function("print"),
      has_output("¡Hola mundo!", pattern = False)
    )
    success_msg("¡Correcto!")
  </code>
  
  <div data-type="hint">
    Usa el símbolo `=` para asignar un valor a una variable y la función <code>print</code> para mostrar el contenido de la variable por pantalla.
  </div>
</div> -->

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio2.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 3

Escribir un programa que pregunte el nombre del usuario en la consola y después de que el usuario lo introduzca muestre por pantalla la cadena `¡Hola <nombre>!`, donde `<nombre>` es el nombre que el usuario haya introducido.

<!-- <div><button class="resolution">Resolver</button></div>
<div data-datacamp-exercise data-lang="python" id="solution" style="display: none">

<code data-type="pre-exercise-code">
    import sys
    from io import StringIO
    sys.stdin = StringIO("input\n")
    del sys
</code>

  <code data-type="sample-code">
    # Preguntar el nombre del usuario y guardarlo en la variable nombre

    # Mostrar por pantalla el saludo con el nombre

  </code>

  <code data-type="solution">
    # Preguntar el nombre del usuario y guardarlo en la variable nombre
    nombre = input("¿Cómo te llamas?")
    # Mostrar por pantalla el saludo con el nombre
    print("Hola " + nombre + "!")
  </code>
  
  <code data-type="sct">
    Ex().multi(
      check_function("input"),
      check_object("nombre"),
      check_function("print"),
      has_output("¡Hola \w+!")
    )
    success_msg("¡Correcto!")
  </code>
  
  <div data-type="hint">
    Usa la función <code>input</code> para leer una cadena desde la terminal, el símbolo `=` para asignar la cadena a la variable y la función <code>print</code> para mostrar el saludo por pantalla.
  </div>
</div> -->

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio3.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 4

Escribir un programa que pregunte el nombre del usuario en la consola y un número entero e imprima por pantalla en líneas distintas el nombre del usuario tantas veces como el número introducido.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio4.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 5

Escribir un programa que pregunte el nombre del usuario en la consola y después de que el usuario lo introduzca muestre por pantalla `<NOMBRE> tiene <n> letras`, donde `<NOMBRE>` es el nombre de usuario en mayúsculas y `<n>` es el número de letras que tienen el nombre.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio5.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 6

Escribir un programa que realice la siguiente operación aritmética $\left(\frac{3+2}{2\cdot 5}\right)^2$.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio6.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 7

Escribir un programa que pregunte al usuario por el número de horas trabajadas y el coste por hora.
Después debe mostrar por pantalla la paga que le corresponde.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio7.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 8

Escribir un programa que lea un entero positivo, $n$, introducido por el usuario y después muestre en pantalla la suma de todos los enteros desde 1 hasta $n$.
La suma de los $n$ primeros enteros positivos puede ser calculada de la siguiente forma:

$$ \mbox{suma} = \frac{n(n+1)}{2} $$

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio7.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 9

Escribir un programa que pida al usuario su peso (en kg) y estatura (en metros), calcule el índice de masa corporal y lo almacene en una variable, y muestre por pantalla la frase `Tu índice de masa corporal es <imc>` donde `<imc>` es el índice de masa corporal calculado redondeado con dos decimales.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio9.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 10

Escribir un programa que pida al usuario dos números enteros y muestre por pantalla la `<n> entre <m> da un cociente <c> y un resto <r>` donde `<n>` y `<m>` son los números introducidos por el usuario, y `<c>` y `<r>` son el cociente y el resto de la división entera respectivamente.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio10.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 11

Escribir un programa que pregunte al usuario una cantidad a invertir, el interés anual y el número de años, y muestre por pantalla el capital obtenido en la inversión.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio11.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 12

Una juguetería tiene mucho éxito en dos de sus productos: payasos y muñecas.
Suele hacer venta por correo y la empresa de logística les cobra por peso de cada paquete así que deben calcular el peso de los payasos y muñecas que saldrán en cada paquete a demanda. Cada payaso pesa 112 g y cada muñeca 75 g.
Escribir un programa que lea el número de payasos y muñecas vendidos en el último pedido y calcule el peso total del paquete que será enviado.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio12.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 13

Imagina que acabas de abrir una nueva cuenta de ahorros que te ofrece el 4% de interés al año. Estos ahorros debido a intereses, que no se cobran hasta finales de año, se te añaden al balance final de tu cuenta de ahorros.
Escribir un programa que comience leyendo la cantidad de dinero depositada en la cuenta de ahorros, introducida por el usuario. Después el programa debe calcular y mostrar por pantalla la cantidad de ahorros tras el primer, segundo y tercer años.
Redondear cada cantidad a dos decimales.  

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio13.ipynb" class="btn btn-info">Solución</a>

## Ejercicio 14

Una panadería vende barras de pan a 3.49€ cada una. El pan que no es el día tiene un descuento del 60%.
Escribir un programa que comience leyendo el número de barras vendidas que no son del día. Después el programa debe mostrar el precio habitual de una barra de pan, el descuento que se le hace por no ser fresca y el coste final total.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/ejercicios/soluciones/tipos-datos/ejercicio14.ipynb" class="btn btn-info">Solución</a>
