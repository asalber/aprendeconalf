---
title: Ejercicios de deshacer cambios
linkTitle: Deshacer cambios
date: 
lastmod:
tags: [Ejercicios]
categories: [Programación, Git]
type: book
weight: 30
---

<i class="fas fa-exclamation-triangle" style="color:red"></i> Para hacer estos ejercicios es necesario haber hecho antes los [ejercicios sobre historial de cambios](/git/ejercicios/historial-cambios.html) o bien hacer un clon del repositorio remoto https://github.com/asalber/libro-git mediante la siguiente secuencia de comandos:

```
> git clone https://github.com/asalber/libro-git.git
> cd libro-git
> git reset --hard 48ed8
> git remote remove origin
```

## Ejercicio 1
1. Eliminar la última línea del fichero `indice.txt` y guardarlo.
2. Comprobar el estado del repositorio.
3. Deshacer los cambios realizados en el fichero `indice.txt` para volver a la versión anterior del fichero.
4. Volver a comprobar el estado del repositorio.

{{< spoiler text="Solución" >}}
```sh
> nano indice.txt
# Eliminar la última línea y guardar el fichero.
> git status
> git checkout -- indice.txt
> git status
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/deshacer-cambios/ejercicio1.gif" />
{{< /spoiler >}}

## Ejercicio 2

1. Eliminar la última línea del fichero `indice.txt` y guardarlo.
2. Añadir los cambios a la zona de intercambio temporal.
3. Comprobar de nuevo el estado del repositorio.
4. Quitar los cambios de la zona de intercambio temporal, pero mantenerlos en el directorio de trabajo.
5. Comprobar de nuevo el estado del repositorio.
6. Deshacer los cambios realizados en el fichero `indice.txt` para volver a la versión anterior del fichero.
7. Volver a comprobar el estado del repositorio.

{{< spoiler text="Solución" >}}
```sh
> nano indice.txt
# Eliminar la última línea y guardar el fichero.
> git add .
> git status
> git reset indice.txt
> git status
> git checkout -- indice.txt
> git status
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/deshacer-cambios/ejercicio2.gif" />
{{< /spoiler >}}

## Ejercicio 3

1. Eliminar la última línea del fichero `indice.txt` y guardarlo.
2. Eliminar el fichero `capitulos/capitulo3.txt`.
3. Añadir un fichero nuevo `captitulos/capitulo4.txt` vacío.
4. Añadir los cambios a la zona de intercambio temporal.
5. Comprobar de nuevo el estado del repositorio.
6. Quitar los cambios de la zona de intercambio temporal, pero mantenerlos en el directorio de trabajo.
7. Comprobar de nuevo el estado del repositorio.
8. Deshacer los cambios realizados para volver a la versión del repositorio.
9. Volver a comprobar el estado del repositorio.

{{< spoiler text="Solución" >}}
```sh
> nano indice.txt
# Eliminar la última línea y guardar el fichero.
> rm capitulos/capitulo3.txt
> touch capitulos/capitulo4.txt
> git add .
> git status
> git reset
> git status
> git checkout -- .
> git status
> git clean -f
> git status
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/deshacer-cambios/ejercicio3.gif" />
{{< /spoiler >}}

## Ejercicio 4

1. Eliminar la última línea del fichero `indice.txt` y guardarlo.
2. Eliminar el fichero `capitulos/capitulo3.txt`.
3. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje "Borrado accidental."
4. Comprobar el historial del repositorio.
5. Deshacer el último commit pero mantener los cambios anteriores en el directorio de trabajo y la zona de intercambio temporal.
6. Comprobar el historial y el estado del repositorio.
7. Volver a hacer el commit con el mismo mensaje de antes.
8. Deshacer el último commit y los cambios anteriores del directorio de trabajo volviendo a la versión anterior del repositorio.
9. Comprobar de nuevo el historial y el estado del repositorio.

{{< spoiler text="Solución" >}}
```sh
> nano indice.txt
# Eliminar la última línea y guardar el fichero.
> rm capitulos/capitulo3.txt
> git commit -a "Borrado accidental."
> git status
> git log
> git reset --soft HEAD~1
> git status
> git commit -m "Borrado accidental."
> git status
> git log
> git reset --hard HEAD~1
> git log
> git status
```
{{< /spoiler >}}
{{< spoiler text="Resolución" >}}
<img src="../soluciones/deshacer-cambios/ejercicio4.gif" />
{{< /spoiler >}}
