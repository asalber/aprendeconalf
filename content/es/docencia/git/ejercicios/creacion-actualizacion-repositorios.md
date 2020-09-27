---
title: Ejercicios de creación y actualización de repositorios
linkTitle: Creación y actualización de repositorios
date: 
lastmod:
tags: [Ejercicios]
categories: [Programación, Git]
type: book
weight: 10
---

## Ejercicio 1

Configurar Git definiendo el nombre del usuario, el correo electrónico y activar el coloreado de la salida. Mostrar la configuración final.

{{< spoiler text="Solución" >}}
```sh
> git config --global user.name "Your-Full-Name"
> git config --global user.email "your-email-address"
> git config --global color.ui auto
> git config --list
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/creacion-actualizacion-repositorios/ejercicio1.gif" />
{{< /spoiler >}}

## Ejercicio 2

Crear un repositorio nuevo con el nombre `libro` y mostrar su contenido.

{{< spoiler text="Solución" >}}
```sh
> mkdir libro
> cd libro
> git init
> ls -la
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/creacion-actualizacion-repositorios/ejercicio2.gif" />
{{< /spoiler >}}

## Ejercicio 3

1. Comprobar el estado del repositorio. 
2. Crear un fichero `indice.txt` con el siguiente contenido:
    
    > Capítulo 1: Introducción a Git  
    > Capítulo 2: Flujo de trabajo básico  
    > Capítulo 3: Repositorios remotos

3. Comprobar de nuevo el estado del repositorio.
4. Añadir el fichero a la zona de intercambio temporal.
5. Volver a comprobar una vez más el estado del repositorio.

{{< spoiler text="Solución" >}}
```sh
> git status
> cat > indice.txt
Capítulo 1: Introducción a Git
Capítulo 2: Flujo de trabajo básico
Capítulo 3: Repositorios remotos
Ctrl+D
> git status
> git add indice.txt
> git status
```
{{< /spoiler >}}
{{< spoiler text="Resolución" >}}
<img src="../soluciones/creacion-actualizacion-repositorios/ejercicio3.gif" />
{{< /spoiler >}}

## Ejercicio 4

Realizar un commit de los últimos cambios con el mensaje "Añadido índice del libro." y ver el estado del repositorio.

{{< spoiler text="Solución" >}}
```sh
> git commit -m "Añadido índice del libro."
> git status
```
{{< /spoiler >}}
{{< spoiler text="Resolución" >}}
<img src="../soluciones/creacion-actualizacion-repositorios/ejercicio4.gif" />
{{< /spoiler >}}

## Ejercicio 5

1. Cambiar el fichero `indice.txt` para que contenga lo siguiente:
    
    > Capítulo 1: Introducción a Git  
    Capítulo 2: Flujo de trabajo básico  
    Capítulo 3: Gestión de ramas  
    Capítulo 4: Repositorios remotos

2. Mostrar los cambios con respecto a la última versión guardada en el repositorio.
3. Hacer un commit de los cambios con el mensaje "Añadido capítulo 3 sobre gestión de ramas".

{{< spoiler text="Solución" >}}
```sh
> cat > indice.txt
Capítulo 1: Introducción a Git
Capítulo 2: Flujo de trabajo básico
Capítulo 3: Gestión de ramas
Capítulo 4: Repositorios remotos
Ctrl+D
> git diff
> git add indice.txt
> git commit -m "Añadido capítulo 3 sobre gestión de ramas"
```
{{< /spoiler >}}
{{< spoiler text="Resolución" >}}
<img src="../soluciones/creacion-actualizacion-repositorios/ejercicio5.gif" />
{{< /spoiler >}}

## Ejercicio 6

1. Mostrar los cambios de la última versión del repositorio con respecto a la anterior.
2. Cambiar el mensaje del último commit por "Añadido capítulo 3 sobre gestión de ramas al índice."
3. Volver a mostrar los últimos cambios del repositorio.

{{< spoiler text="Solución" >}}
```sh
> git show
> git commit --amend -m "Añadido capítulo 3 sobre gestión de ramas al índice."
git show
```
{{< /spoiler >}}
{{< spoiler text="Resolución" >}}
<img src="../soluciones/creacion-actualizacion-repositorios/ejercicio6.gif" />
{{< /spoiler >}}
