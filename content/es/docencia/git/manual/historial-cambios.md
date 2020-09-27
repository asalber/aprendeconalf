---
title: Historial de cambios
lastmod: 
tags: 
categories: [Programación, Git]
type: book
weight: 30
---

## Estado e historia de un repositorio

### Mostrar el estado de un repositorio

#### `git status`

- `git status` muestra el estado de los cambios en el repositorio desde la última versión guardada. En particular, muestra los ficheros con cambios en el directorio de trabajo que no se han añadido a la zona de intercambio temporal y los ficheros en la zona de intercambio temporal que no se han añadido al repositorio.

### Mostrar el historial de versiones de un repositorio

#### `git log`

- `git log` muestra el historial de commits de un repositorio ordenado cronológicamente. Para cada commit muestra su código hash, el autor, la fecha, la hora y el mensaje asociado.  
Este comando es muy versátil y muestra la historia del repositorio en distintos formatos dependiendo de los parámetros que se le den. Los más comunes son:
    - `--oneline` muestra cada commit en una línea produciendo una salida más compacta.
    - `--graph` muestra la historia en forma de grafo.

### Mostrar los datos de un commit

#### `git show`

- `git show` muestra el usuario, el día, la hora y el mensaje del último commit, así como las diferencias con el anterior.

- `git show <commit>` muestra el usuario, el día, la hora y el mensaje del commit indicado, así como las diferencias con el anterior.

### Mostrar el historial de cambios de un fichero

#### `git annotate`

- `git annotate` muestra el contenido de un fichero anotando cada línea con información del commit en el que se introdujo.  
Cada línea de la salida contiene los 8 primeros dígitos del código hash del commit correspondiente al cambio, el autor de los cambio, la fecha, el número de línea del fichero y el contenido de la línea.

## Mostrar las diferencias entre versiones

#### `git diff`

- `git diff` muestra las diferencias entre el directorio de trabajo y la zona de intercambio temporal.

- `git diff --cached` muestra las diferencias entre la zona de intercambio temporal y el último commit.

- `git diff HEAD` muestra la diferencia entre el directorio de trabajo y el último commit.
