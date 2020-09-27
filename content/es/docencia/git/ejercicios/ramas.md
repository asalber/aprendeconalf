---
title: Ejercicios de gestión de ramas
linkTitle: Ramas
date: 
lastmod:
tags: [Ejercicios]
categories: [Programación, Git]
type: book
weight: 40
---
<i class="fas fa-exclamation-triangle" style="color:red"></i> Para hacer estos ejercicios es necesario haber hecho antes los [ejercicios sobre historial de cambios](/git/ejercicios/historial-cambios.html) o bien hacer un clon del repositorio remoto https://github.com/asalber/libro-git mediante la siguiente secuencia de comandos:

```
> git clone https://github.com/asalber/libro-git.git
> cd libro-git
> git reset --hard 48ed8
> git remote remove origin
```

## Ejercicio 1
Crear una nueva rama `bibliografia` y mostrar las ramas del repositorio.

{{< spoiler text="Solución" >}}
```sh
> git branch bibliografia
> git branch -av
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/ramas/ejercicio1.gif" />
{{< /spoiler >}}

## Ejercicio 2

1. Crear el fichero `capitulos/capitulo4.txt` y añadir el texto siguiente
> En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.

2. Añadir los cambios a la zona de intercambio temporal.
3. Hacer un commit con el mensaje "Añadido capítulo 4."
4. Mostrar la historia del repositorio incluyendo todas las ramas.

{{< spoiler text="Solución" >}}
```sh
> cat > capitulos/capitulo4.txt
En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
Ctrl+D
> git add .
> git commit -m "Añadido capítulo 4."
> git log --graph --all --oneline
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/ramas/ejercicio2.gif" />
{{< /spoiler >}}

## Ejercicio 3

1. Cambiar a la rama `bibliografia`.
2. Crear el fichero `bibliografia.txt` y añadir la siguiente referencia
> - Chacon, S. and Straub, B. Pro Git. Apress.

3. Añadir los cambios a la zona de intercambio temporal.
4. Hacer un commit con el mensaje "Añadida primera referencia bibliográfica."
5. Mostrar la historia del repositorio incluyendo todas las ramas.

{{< spoiler text="Solución" >}}
```sh
> git checkout bibliografia
> cat > bibliografia.txt
- Chacon, S. and Straub, B. Pro Git. Apress.
Ctrl+D
> git add .
> git commit -m "Añadida primera referencia bibliográfica."
> git log --graph --all --oneline
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/ramas/ejercicio3.gif" />
{{< /spoiler >}}

## Ejercicio 4

1. Fusionar la rama `bibliografia` con la rama `master`.
2. Mostrar la historia del repositorio incluyendo todas las ramas.
3. Eliminar la rama `bibliografia`. 
4. Mostrar de nuevo la historia del repositorio incluyendo todas las ramas.

{{< spoiler text="Solución" >}}
```sh
> git checkout master
> git merge bibliografia
> git log --graph --all --oneline
> git branch -d bibliografia
> git log --graph --all --oneline
```
{{< /spoiler >}}
{{< spoiler text="Resolución" >}}
<img src="../soluciones/ramas/ejercicio4.gif" />
{{< /spoiler >}}

## Ejercicio 5

1. Crear la rama `bibliografia`.
2. Cambiar a la rama `bibliografia`.
3. Cambiar el fichero `bibliografia.txt` para que contenga las siguientes referencias: 
> - Scott Chacon and Ben Straub. Pro Git. Apress.
> - Ryan Hodson. Ry's Git Tutorial. Smashwords (2014)

4. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje "Añadida nueva referencia bibliográfica."
5. Cambiar a la rama `master`.
6. Cambiar el fichero `bibliografia.txt` para que contenga las siguientes referencias: 
> - Chacon, S. and Straub, B. Pro Git. Apress.
> - Loeliger, J. and McCullough, M. Version control with Git. O'Reilly.

7. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje "Añadida nueva referencia bibliográfica."
8. Fusionar la rama `bibliografia` con la rama `master`.
9. Resolver el conflicto dejando el fichero `bibliografia.txt` con las referencias:
> - Chacon, S. and Straub, B. Pro Git. Apress.
> - Loeliger, J. and McCullough, M. Version control with Git. O'Reilly.
> - Hodson, R. Ry's Git Tutorial. Smashwords (2014)
10. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje "Resuelto conflicto de bibliografía."
11. Mostrar la historia del repositorio incluyendo todas las ramas.

{{< spoiler text="Solución" >}}
```sh
> git branch bibliografia
> git checkout bibliografia
> cat > bibliografia.txt
- Scott Chacon and Ben Straub. Pro Git. Apress.
- Ryan Hodson. Ry's Git Tutorial. Smashwords (2014)
Ctrl+D
> git commit -a -m "Añadida nueva referencia bibliográfica."
> git checkout master
> cat > bibliografia.txt
- Chacon, S. and Straub, B. Pro Git. Apress.
- Loeliger, J. and McCullough, M. Version control with Git. O'Reilly.
Ctrl+D
> git commit -a -m "Añadida nueva referencia bibliográfica."
> git merge bibliografia
> git nano bibliografia
# Hacer los cambios indicados en el fichero
> git commit -a -m "Solucionado conflicto bibliografía."
> git log --graph --all --oneline
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/ramas/ejercicio5.gif" />
{{< /spoiler >}}