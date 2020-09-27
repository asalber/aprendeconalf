---
title: Ejercicios de manejo del historial de cambios
linkTitle: Historial de cambios
date: 
lastmod:
tags: [Ejercicios]
categories: [Programación, Git]
type: book
weight: 20
---

<i class="fas fa-exclamation-triangle" style="color:red"></i> Para hacer estos ejercicios es necesario haber hecho antes los  [ejercicios de creación y actualización de repositorios](/git/ejercicios/creacion-actualizacion-repositorios.html) o bien hacer un clon del repositorio remoto https://github.com/asalber/libro-git mediante la siguiente secuencia de comandos:

```sh
> git clone https://github.com/asalber/libro-git.git
> cd libro-git
> git reset --hard 8c808
> git remote remove origin
```

## Ejercicio 1
1. Mostrar el historial de cambios del repositorio.
2. Crear la carpeta `capitulos` y crear dentro de ella el fichero `capitulo1.txt` con el siguiente texto.
    > Git es un sistema de control de versiones ideado por Linus Torvalds.
3. Añadir los cambios a la zona de intercambio temporal.
4. Hacer un commit de los cambios con el mensaje "Añadido capítulo 1."
5. Volver a mostrar el historial de cambios del repositorio.

{{< spoiler text="Solución" >}}
```sh
> git log
> mkdir capitulos
> cat > capitulos/capitulo1.txt
Git es un sistema de control de versiones ideado por Linus Torvalds.
Ctrl+D
> git add .
> git commit -m "Añadido capítulo 1."
> git log
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/historial-cambios/ejercicio1.gif" />
{{< /spoiler >}}

## Ejercicio 2

1. Crear el fichero `capitulo2.txt` en la carpeta `capitulos` con el siguiente texto.
    > El flujo de trabajo básico con Git consiste en:
    1- Hacer cambios en el repositorio.
    2- Añadir los cambios a la zona de intercambio temporal.
    3- Hacer un commit de los cambios.
2. Añadir los cambios a la zona de intercambio temporal.
3. Hacer un commit de los cambios con el mensaje "Añadido capítulo 2."
4. Mostrar las diferencias entre la última versión y dos versiones anteriores.

{{< spoiler text="Solución" >}}
```sh
> cat > capitulos/capitulo2.txt
El flujo de trabajo básico con Git consiste en:
1- Hacer cambios en el repositorio.
2- Añadir los cambios a la zona de intercambio temporal.
3- Hacer un commit de los cambios.
Ctrl+D
> git add .
> git commit -m "Añadido capítulo 2."
> git diff HEAD~2..HEAD
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/historial-cambios/ejercicio2.gif" />
{{< /spoiler >}}

## Ejercicio 3

1. Crear el fichero `capitulo3.txt` en la carpeta `capitulos` con el siguiente texto.
    > Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
2. Añadir los cambios a la zona de intercambio temporal.
3. Hacer un commit de los cambios con el mensaje "Añadido capítulo 3."
4. Mostrar las diferencias entre la primera y la última versión del repositorio.

{{< spoiler text="Solución" >}}
```sh
> cat > capitulos/capitulo3.txt
Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
Ctrl+D
> git add .
> git commit -m "Añadido capítulo 3."
> git log
> git diff &lt;codigo hash de la primera version>..HEAD
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/historial-cambios/ejercicio3.gif" />
{{< /spoiler >}}

## Ejercicio 4

1. Añadir al final del fichero `indice.txt` la siguiente línea:
    
    > Capítulo 5: Conceptos avanzados

2. Añadir los cambios a la zona de intercambio temporal.
3. Hacer un commit de los cambios con el mensaje "Añadido capítulo 5 al índice.".
4. Mostrar quién ha hecho cambios sobre el fichero `indice.txt`.

{{< spoiler text="Solución" >}}
```sh
> echo "Capítulo 5: Conceptos avanzados" >> indice.txt
> git add .
> git commit -m "Añadido capítulo 5 al índice."
> git annotate indice.txt
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/creacion-actualizacion-repositorios/ejercicio4.gif" />
{{< /spoiler >}}
