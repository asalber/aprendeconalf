---
title: Introducción a Git
lastmod: 
tags:
categories: [Programación, Git]
type: book
weight: 10
---

## ¿Qué es un sistema de control de versiones?

{{% alert def %}}
Un **Sistema de Control de Versiones** (SCV) es una aplicación que permite gestionar los cambios que se realizan sobre los elementos de un proyecto o repositorio, guardando así versiones del mismo en todas sus fases de desarrollo.
{{% /alert %}}

- Registra cada cambio en el proyecto o repositorio, quién y cuándo lo hace, en una base de datos.
- Permite volver a estados previos del desarrollo.
- Permite gestionar diferentes versiones del proyecto (ramas) para trabajar en paralelo y luego fundirlas.
- Permite colaborar entre diferentes usuarios en un mismo repositorio, facilitando la resolución de conflictos.
- Se utiliza principalmente en proyectos de desarrollo de software, pero sirve para cualquier otro tipo de proyecto.

## ¿Qué es Git?

**Git** es un sistema de control de versiones de código abierto ideado por Linus Torvalds (el padre del sistema operativo Linux) y actualmente es el sistema de control de versiones más extendido.

A diferencia de otros SCV Git tiene una arquitectura _distribuida_, lo que significa que en lugar de guardar todos los cambios de un proyecto en un único sitio, cada usuario contiene una copia del repositorio con el historial de cambios completo del proyecto. Esto aumenta significativamente su rendimiento.

<img src="../img/logo-git.png" alt="Logo de Git">

## Configuración de Git

Antes de empezar a usar git es necesario configurarlo con el nombre de usuario y su correo electrónico.

#### `git config`

- Establecer el nombre de usuario
```sh
git config --global user.name "Your-Full-Name"
```
- Establecer el correo del usuario
```sh
git config --global user.email "your-email-address"
```
- Activar el coloreado de la salida
```sh
git config --global color.ui auto
```
- Mostrar el estado original en los conflictos
```sh
git config --global merge.conflictstyle diff3
```
- Mostrar la configuración
```sh
git config --list
```