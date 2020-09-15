---
title: Examen de Inteligencia de los Negocios 2019-03-27
date: 2019-03-27
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 27 de Marzo de 2019

## Ejercicio 1

1. Clonar con git el repositorio con la url `https://github.com/asalberceu/examen-fundamentos-programacion-2019-03-27-A.git`.
2. Crear una rama con los apellidos del alumno en mayúsculas y separados por un guión, es decir, `APELLIDO1-APELLIDO2`, y convertir esta rama en la rama activa.
3. Crear la carpeta `respuestas`, y dentro de ella el fichero `ejercicio1.3.txt` que contenga la salida que da el comando de Git para mostrar todas diferencias entre la última versión de la rama actual y la anterior.
4. Añadir todos los cambios a la zona temporal de intercambio y hacer un commit con el mensaje "Añadida respuesta ejercicio 1.3."
5. Crear dentro de la carpeta `respuestas` el fichero `ejercicio1.5.txt` que contenga la salida que da el comando de Git para mostrar todos los commits del repositorio (una línea por commit), incluyendo todas las ramas.
6. Añadir todos los cambios a la zona temporal de intercambio y hacer un commit con el mensaje "Añadida respuesta ejercicio 1.5."

{{< spoiler text="Solución" >}} 
```sh
> git clone https://github.com/asalberceu/examen-fundamentos-programacion-2019-03-27-A.git
> cd examen-fundamentos-programacion-2019-03-27-A
> git checkout -b SANCHEZ-ALBERCA
> mkdir respuestas
> git diff HEAD~1 > respuestas/ejercicio1.3.txt
> git add .
> git commit -m "Añadida respuesta ejercicio 1.3"
> git log --oneline --all > respuestas/ejercicio1.5.txt
> git add .
> git commit -m "Añadida respuesta ejercicio 1.5"
```
{{< /spoiler >}}

## Ejercicio 2

Escribir un programa que realice la devolución de una cantidad dada por el usuario en monedas.

El programa debe cumplir los siguientes requisitos:

- Solo se disponen de tres tipos de monedas: 5, 2 y 1 €. Crear una lista que contenga estos tres tipos de moneda y usar la lista en la solución.
- El programa debe preguntar al usuario por una cantidad entera de euros.
- El programa debe mostrar por pantalla el mínimo número de monedas necesarias para sumar la cantidad introducida por el usuario y cuántas monedas de cada tipo se necesitan para ello. El número de monedas de cada tipo debe guardarse en otra lista.
- El programa debe guardarse dentro de la carpeta `respuestas` con el nombre `ejercicio2.py`.
- Cuando el programa esté terminado, añadir el fichero `ejercicio2.py` a la zona de intercambio temporal y hacer un commit con el mensaje "Añadida respuesta ejercicio 2".

<a href="https://repl.it/@asalber/examen-2019-03-27-ejercicio-2" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Escribir un programa que simule el famoso juego del ahorcado.

El programa debe cumplir los siguientes requisitos:

- El programa debe preguntar al usuario la palabra a adivinar. A partir de la palabra introducida debe crear una lista con los caracteres de la palabra.
- Después debe ir preguntando al usuario por letras hasta un máximo de 5 fallos o hasta que no queden letras en la lista. En ambos casos el programa terminará pero mostrará el mensaje "Perdiste" si se comenten 5 fallos y el mensaje "Ganaste" si no quedan palabras en la lista.
- Cada vez que el usuario introduzca una nueva letra, si la letra está en la lista la eliminará y mostrará el mensaje "Acierto", mientras que si la letra no está en la lista mostrará el mensaje "Fallo". Si la letra está más de una vez en la lista, sólo se eliminará la primera instancia que aparezca.
- El programa debe guardarse dentro de la carpeta `respuestas` con el nombre `ejercicio3.py`.
- Cuando el programa esté terminado, añadir el fichero `ejercicio3.py` a la zona de intercambio temporal y hacer un commit con el mensaje "Añadida respuesta ejercicio 3".

Requisito adicional para un punto extra:

- Cada vez que el usuario acierte una letra debe mostrar la palabra a adivinar con las letras acertadas hasta el momento y el resto reemplazadas por asteriscos.

<a href="https://repl.it/@asalber/examen-2019-03-27-ejercicio-3" class="btn btn-info" target="_blank">Solución</a>
