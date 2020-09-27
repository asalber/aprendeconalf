---
title: Repositorios remotos
lastmod: 
tags:
categories: [Programación, Git]
type: book
weight: 60
---

## Repositorios remotos

La otra característica de Git, que unida a las ramas, facilita la colaboración entre distintos usuarios en un proyecto son los repositorios remotos.

Git permite la creación de una copia del repositorio en un servidor git en internet. La principal ventaja de tener una copia remota del repositorio, a parte de servir como copia de seguridad, es que otros usuarios pueden acceder a ella y hacer también cambios.

Existen muchos proveedores de alojamiento para repositorios Git pero el más usado es GitHub.

### ¿Qué es GitHub?

**GitHub** es el proveedor de alojamiento en la nube para repositorios gestionados con git más usado y el que actualmente tiene alojados más proyectos de desarrollo de software de código abierto en el mundo.

La principal ventaja de GitHub es que permite albergar un número ilimitado de repositorios tanto públicos como privados, y que además ofrece servicios de registro de errores, solicitud de nuevas funcionalidades, gestión de tareas, wikis o publicación de páginas web, para cada proyecto, incluso con el plan básico que es gratuito.

<img src="../img/logo-github.jpeg" alt="Logo de GitHub">

### Añadir un repositorio remoto

#### `git remote add`

- `git remote add <repositorio-remoto> <url>` crea un enlace con el nombre `<repositorio-remoto>` a un repositorio remoto ubicado en la dirección `<url>`.

Cuando se añade un repositorio remoto a un repositorio, Git seguirá también los cambios del repositorio remoto de manera que se pueden descargar los cambios del repositorio remoto al local y se pueden subir los cambios del repositorio local al remoto.

### Lista de repositorios remotos

#### `git remote`

- `git remote` muestra un listado con todos los enlaces a repositorios remotos definidos en un repositorio local.

- `git remote -v` muestra además las direcciones url para cada repositorio remoto.

### Descargar cambios desde un repositorio remoto

#### `git pull`

- `git pull <remoto> <rama>` descarga los cambios de la rama `<rama>` del repositorio remoto `<remoto>` y los integra en la última versión del repositorio local, es decir, en el HEAD.

- `git fetch <remoto>` descarga los cambios del repositorio remoto `<remoto>` pero no los integra en la última versión del repositorio local.

### Subir cambios a un repositorio remoto

#### `git push`

- `git push <remoto> <rama>` sube al repositorio remoto `<remoto>` los cambios de la rama `<rama>` en el repositorio local.

### Colaboración en repositorios remotos de GitHub

Existen dos formas de colaborar en un repositorio alojado en GitHub:

- Ser colaborador del repositorio.
    1. Recibir autorización de colaborador por parte de la persona propietaria del proyecto.
    2. Clonar el repositorio en local.
    3. Hacer cambios en el repositorio local.
    4. Subir los cambios al repositorio remoto. Primero hacer `git pull` para integrar los cambios remotos en el repositorio local y luego `git push` para subir los cambios del repositorio local al remoto.

- Replicar el repositorio y solicitar integración de cambios.
    1. Replicar el repositorio remoto en nuestra cuenta de GitHub mediante un `fork`.
    2. Hacer cambios en nuestro repositorio remoto.
    3. Solicitar a la persona propietaria del repositorio original que integre nuestros cambios en su repositorio mediante un `pull request`.
