---
title: Deshacer cambios
lastmod: 
tags:
categories: [Programación, Git]
type: book
weight: 40
---

## Deshacer cambios

### Eliminar cambios del directorio de trabajo o volver a una versión anterior

#### `git checkout`

- `git checkout <commit> -- <file>` actualiza el fichero `<file>` a la versión correspondiente al commit `<commit>`.  
Suele utilizarse para eliminar los cambios en un fichero que no han sido guardados aún en la zona de intercambio temporal, mediante el comando `git checkout HEAD -- <file>`.

### Eliminar cambios de la zona de intercambio temporal

#### `git reset`

- `git reset <fichero>` elimina los cambios del fichero `<fichero`> de la zona de intercambio temporal, pero preserva los cambios en el directorio de trabajo.

Para eliminar por completo los cambios de un fichero que han sido guardados en la zona de intercambio temporal hay que aplicar este comando y después `git checkout HEAD -- <fichero>`.

### Eliminar cambios de un commit

#### `git reset`

- `git reset --hard <commit>` elimina todos los cambios desde el commit `<commit>` y actualiza el HEAD este commit.  
   
  Suele usarse para eliminar todos los cambios en el directorio de trabajo desde el último commit mediante el comando `git reset --hard HEAD`.

  {{% alert warning %}}
Usar con cuidado este comando pues los cambios posteriores al commit indicado se pierden por completo.
{{% /alert %}}

- `git reset <commit>` actualiza el HEAD al commit `<commit>`, es decir, elimina todos los commits posteriores a este commit, pero no elimina los cambios del directorio de trabajo.
