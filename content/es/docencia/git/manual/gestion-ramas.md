---
title: Gestión de ramas
lastmod: 
tags:
categories: [Programación, Git]
type: book
weight: 50
---

## Ramas

Inicialmente cualquier repositorio tiene una única rama llamada **master** donde se van sucediendo todos los commits de manera lineal.

Una de las característica más útiles de Git es que permite la creación de ramas para trabajar en distintas versiones de un proyecto a la vez.

Esto es muy útil si, por ejemplo, se quieren añadir nuevas funcionalidades al proyecto sin que interfieran con lo desarrollado hasta ahora.

Cuando se termina el desarrollo de las nuevas funcionalidades las ramas se pueden fusionar para incorporar lo cambios al proyecto principal.

### Creación de ramas

#### `git branch`

- `git branch <rama>` crea una nueva rama con el nombre `<rama>` en el repositorio a partir del último commit, es decir, donde apunte HEAD.

Al crear una rama a partir de un commit, el flujo de commits se bifurca en dos de manera que se pueden desarrollar dos versiones del proyecto en paralelo.

<img src="../img/ramificacion.png" alt="Dos ramas del repositorio git">

### Desarrollo en ramas diferentes

<img src="../img/dos-ramas.png" alt="Dos ramas del repositorio git">

### Listado de ramas

#### `git log`

- `git branch` muestra las ramas activas de un repositorio indicando con __*__ la rama activa en ese momento.  

- `git log --graph --oneline` muestra la historia del repositorio en forma de grafo (--graph) incluyendo todas las ramas (--all).

### Cambio de ramas

#### `git checkout`

- `git checkout <rama>` actualiza los ficheros del directorio de trabajo a la última versión del repositorio correspondiente a la rama `<rama>`, y la activa, es decir, HEAD pasa a apuntar al último commit de esta rama.

- `git checkout -b <rama>` crea una nueva rama con el nombre `<rama>` y la activa, es decir, HEAD pasa a apuntar al último commit de esta rama. Este comando es equivalente aplicar los comandos `git branch <rama>` y después `git checkout <rama>`.

### Fusión de ramas

#### `git merge`

- `git merge <rama>` integra los cambios de la rama `<rama>` en la rama actual a la que apunta HEAD.

<img src="../img/fusion-ramas.png" alt="Dos ramas del repositorio git">

### Resolución de conflictos

Para fusionar dos ramas es necesario que no haya conflictos entre los cambios realizados a las dos versiones del proyecto.

Si en ambas versiones se han hecho cambios sobre la misma parte de un fichero, entonces se produce un conflicto y es necesario resolverlo antes de poder fusionar las ramas.

La resolución debe hacerse manualmente observando los cambios que interfieren y decidiendo cuales deben prevalecer, aunque existen herramientas como KDif3 o meld que facilitan el proceso.

### Reorganización de ramas

#### `git rebase`

- `git rebase <rama-1> <rama-2>` replica los cambios de la rama `<rama-2>` en la rama `<rama-1>` partiendo del ancestro común de ambas ramas.
El resultado es el mismo que la fusión de las dos ramas pero la bifurcación de la `<rama-2>` desaparece ya que sus commits pasan a estar en la `<rama-1>`.

### Eliminación de ramas

#### `git branch -d`

- `git branch -d <rama>` elimina la rama de nombre `<rama>` siempre y cuando haya sido fusionada previamente.

- `git branch -D <rama>` elimina la rama de nombre `<rama>` incluso si no ha sido fusionada. Si la rama no ha sido fusionada previamente se perderán todos los cambios de esa rama.
