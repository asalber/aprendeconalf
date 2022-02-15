---
title: Terminal de sistemas MacOs
subtitle: 
summary: Comandos más habituales para la shell zsh
lastmod: 
tags: [Herramientas]
categories: [Programación, Python]
type: book
---

El sistema de archivos del sistema operativo MacOs es muy parecida a la de los sistemas Linux y organiza el contenido de todos los discos duros y sistemas de almacenamiento siguiendo una estructura de árbol cuya raíz es siempre el directorio principal que se representa como la barra diagonal `/`. El directorio principal contiene todos los archivos del sistema.

Por otro lado, cada usuario del sistema tiene asignado un directorio principal de usuario que está dentro del directorio `/Users` y se representa con el carácter `~`. Cualquier usuario puede hacer los cambios que quiera en su directorio de usuario pero no podrá acceder los directorios de otros usuarios ni del resto del sistema de archivos salvo que tenga permiso de administrador del sistema (root).

![Estructura de directorios del sistema operativo MacOs](img/sistema-archivos-macos.png)

## Rutas absolutas y relativas

La ubicación de un archivo o un directorio en la estructura de árbol de la unidad se puede determinar mediante una ruta absoluta o una ruta relativa.

La **ruta absoluta** de un archivo o directorio es la secuencia de directorios que hay que atravesar para llegar al archivo o directorio en cuestión desde el directorio raíz. La ruta se expresa separando los directorios con la barra diagonal `/`.

La **ruta relativa** de un archivo o directorio es la secuencia de directorios que hay que atravesar para llegar al archivo o directorio en cuestión desde el directorio activo. Para referirse al directorio madre se utiliza el alias `..`, mientras que para referirse al propio directorio activo se utiliza el alias `.`.

Mientras que la ruta absoluta de un archivo o directorio es única, la ruta relativa depende del directorio activo.

**Ejemplo**. Supongamos el siguiente árbol de directorios.

![Ejemplo de árbol de archivos](img/arbol-archivos.svg)

La ruta absoluta al directorio `Programación` sería `/Users/Alumno/Grado/Primero/Programación`, mientras que la ruta relativa, asumiendo que el directorio activo es `Primero`, es `./Programación`.
Del mismo modo, la ruta relativa hasta el directorio `Segundo` sería `../Segundo`.

## La terminal de los sistemas MacOs

La terminal de los sistemas MacOs proporciona una interfaz de línea de comando (CLI) para acceder a los archivos y dar instrucciones al sistema.

La aplicación `Terminal` viene instalada por defecto en los sistemas MacOs y puede ejecutarse como cualquier otra aplicación desde el Launchpad. Cuando se ejecuta abre una ventana de texto muestra la fecha de la última conexión y el `prompt`, que es una cadena de texto que incluye el nombre del usuario, el nombre del ordenador y la ruta del directorio actual (inicialmente el directorio principal del usuario `~`) terminada con el carácter `%`. A partir de aquí el usuario puede dar ordenes al sistema tecleando comandos. 

El programa encargado de interpretar los comandos que el usuario introduce en la terminal se denomina `shell` y en las últimas versiones de MacOs por defecto se utiliza la [shell zsh](https://es.wikipedia.org/wiki/Zsh). 

## Comandos básicos de la shell zsh

Un comando es una instrucción a ejecutar por el sistema operativo. Los comandos suelen llevar asociados parámetros y argumentos. Los parámetros modifican la manera de realizar la instrucción y van precedidos de un guión `-` o un doble guión `--`, mientras que los argumentos indican sobre qué objeto se realiza la acción de indica la instrucción (un archivo, un directorio, etc.)

|Comando | Acción
|:---|:---|
|`ls` | Muestra un listado con el contenido del directorio actual.|
|`ls -l` | Muestra un listado detallado con el contenido del directorio actual.|
|`ls -la`| Muestra un listado detallado con el contenido del directorio actual, incluyendo os archivos ocultos.
|`ls <dir>` | Muestra un listado del directorio `<dir>`.|
|`cd <dir>` | Cambia al directorio `<dir>` convirtiéndolo en el directorio activo.|
|`mkdir <dir>` | Crea el directorio `<dir>`.|
|`mv <origen> <destino>` | Mueve el archivo o directorio `<origen>` al directorio `<destino>`.|
|`rm <f>` | Elimina el archivo `<f>`. |
|`rm -r <dir>` | Elimina el directorio `<dir>` y todo su contenido.|

## Trucos de la terminal

Para manejar con soltura la terminal conviene utilizar algunos trucos que facilitan su uso. 

- Tabulador. La tecla tabulador (⇥) permite completar la entrada del usuario automáticamente, es decir, el usuario comienza a teclear un comando o ruta de archivo y, sin necesidad de escribirla por completo, cuando se pulsa la tecla tabulador el sistema intenta completarla siempre y cuando no haya más de un comando o ruta que comiencen por esos caracteres.

- Teclas de desplazamiento. Las teclas con las flechas de desplazamiento arriba (↑) y abajo (↓) permiten reutilizar comandos que se han usado previamente en la misma sesión de la terminal. 

- Limpiar la terminal. La combinación de las teclas `Ctr` + `l` limpia la terminal. 