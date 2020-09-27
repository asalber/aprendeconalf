---
title: Ejercicios de repositorios remotos
linkTitle: Repositorios remotos
date: 
lastmod:
tags: [Ejercicios]
categories: [Programación, Git]
type: book
weight: 50
---

<i class="fas fa-exclamation-triangle" style="color:red"></i> Para hacer estos ejercicios es necesario haber hecho antes los [ejercicios sobre ramas](/git/ejercicios/ramas.html) o bien hacer un clon del repositorio remoto https://github.com/asalber/libro-git mediante la siguiente secuencia de comandos:

```sh
> git clone https://github.com/asalber/libro-git.git
> cd libro-git
> git reset --hard cb1e4
> git remote remove origin
```

## Ejercicio 1
1. Crear un nuevo repositorio público en GitHub con el nombre `libro-git`.
2. Añadirlo al repositorio local del libro.
3. Mostrar todos los repositorios remotos configurados.

{{< spoiler text="Solución" >}}
```sh
# Crear el repositorio en GitHub y copiar su url con protocolo https.
> git remote add github url
> git remote -v
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/repositorios-remotos/ejercicio1.gif" />
{{< /spoiler >}}

## Ejercicio 2

1. Añadir los cambios del repositorio local al repositorio remoto de GitHub.
2. Acceder a GitHub y comprobar que se han subido los cambios mostrando el historial de versiones.

{{< spoiler text="Solución" >}}
```sh
>git push github master
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/repositorios-remotos/ejercicio2.gif" />
{{< /spoiler >}}

## Ejercicio 3

1. Colaborar en el repositorio remoto `libro-git` de otro usuario.
2. Clonar su repositorio `libro-git`.
3. Añadir el fichero `autores.txt` que contenga el nombre del usuario y su correo electrónico.
4. Añadir los cambios a la zona de intercambio temporal.
5. Hacer un commit con el mensaje "Añadido autor."
6. Subir los cambios al repositorio remoto.

{{< spoiler text="Solución" >}}
```sh
# Entrar en GigHub en el proyecto libro-git del que seamos colaboradores y copiar la url.
> git clone url
> cat > autores.txt
# Escribir el nombre del autor y su correo.
Ctrl+D
> git add .
> git commit -m "Añadido autor."
> git push origin master.
```
{{< /spoiler >}}

{{< spoiler text="Resolución" >}}
<img src="../soluciones/repositorios-remotos/ejercicio3.gif" />
{{< /spoiler >}}

## Ejercicio 4

1. Hacer una bifurcación del repositorio remoto `asalber/libro-git` en GitHub.
2. Clonar el repositorio creado en la cuenta de GitHub del usuario.
3. Crear una nueva rama `autoria` y activarla.
4. Añadir el nombre del usuario y su correo al fichero `autores.txt`.
5. Añadir los cambios a la zona de intercambio temporal.
6. Hacer un commit con el mensaje "Añadido nuevo autor."
7. Subir los cambios de la rama `autoria` al repositorio remoto en GitHub.
8. Hacer un Pull Request de los cambios en la rama `autoria`.

{{< spoiler text="Solución" >}}
```sh
# Hacer el fork del repositorio asalber/libro-git en GitHub y copiar la url del repositorio creado en la cuenta de GitHub del usuario.
> git clone url
> git checkout -b autoria
# Editar con nano el fichero autores.txt y añadir el nombre y el correo electrónico del usuario en una nueva línea.
> git commit -am "Añadido nuevo autor."
> git push origin autoria
# Ir al repositorio remoto en GitHub y hacer clic en el botón Compare & Pull Request y después completar la solicitud haciendo clic en el botón Create Pull Request.
```
{{< /spoiler >}}
{{< spoiler text="Resolución" >}}
<img src="../soluciones/repositorios-remotos/ejercicio4.gif" />
{{< /spoiler >}}
