---
title: Ejercicios de $\LaTeX$
summary: Ejercicios de resueltos.
linkTitle: 
date: 
lastmod:
tags: [Ejercicios]
categories: [LaTeX]
type: book
weight: 10
---

## Ejercicio 1

Escribir el código LaTeX para generar el siguiente [documento](doc/ejercicio1.pdf), pero con la fecha actual.

{{< spoiler text="Solución" >}}
```latex
% CLASE
\documentclass[a4paper,12pt]{article}
% PREÁMBULO
% Paquetes
\usepackage{fontspec}
\usepackage{polyglossia}
\setdefaultlanguage{spanish}

% Título, autor y fecha
\title{Hola Mundo}
\author{Alfredo Sánchez Alberca}
\date{\today}

\begin{document}
\maketitle

\textbf{¡Hola Mundo!} Hoy empiezo a aprender \LaTeX.
\end{document}
```
{{< /spoiler >}}

## Ejercicio 2

Escribir el código LaTeX para generar el siguiente [documento](doc/ejercicio2.pdf).

{{< spoiler text="Solución" >}}
```TeX
% CLASE
\documentclass[a4paper,12pt]{article}

% PREÁMBULO
% Paquetes
\usepackage{fontspec}
\usepackage{polyglossia}
\setdefaultlanguage{spanish}

% Título, autor y fecha
\title{Curso de \LaTeX}
\author{María López \and Juan Sánchez}
\date{}

% CUERPO
\begin{document}
\maketitle
\tableofcontents

\section{Introducción}

LaTeX es un sistema de composición de textos, orientado especialmente a la creación de documentos científicos y técnicos que contengan fórmulas matemáticas.

\subsection{Código abierto}

LaTeX es un programa de \emph{código abierto} por lo que cualquier usuario puede modificar el código y adaptarlo a sus necesidades.

\subsection{Distribuciones}

Existen distribuciones de LaTeX para la mayoría de los sistemas operativos. Las más conocidas son TexLive, MikTex y MacTex.

\section{Paquetes}

Existen multitud de paquetes de macros en LaTeX para realizar diversas tareas desde gráficos hasta composición de partituras. El principal repositorio de paquetes es CRAN( \texttt{https://cran.r-project.org/})

\end{document}
```
{{< /spoiler >}}

## Ejercicio 3

Escribir el código LaTeX para generar las siguientes fórmulas:

a. $$\int_a^b x dx = \left.\frac{x^2}{2} \right|_a^b$$

b. $$\frac{dy}{dx}=y'=\lim_{h \to 0}\frac{f(x+h)-f(x)}{h}$$

c. $$\sum_n \frac{1}{n^s}=\prod_p \frac{1}{1-\frac{1}{p^s}}$$

d. $$\nabla f(x,y,z) = \left(\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z}\right)$$

e. $$\frac{1+\frac{a}{b}}{1+\ln{\frac{\sqrt{b^2}}{1+\frac{1}{a}}}}$$

{{< spoiler text="Solución" >}}
a. `$$\int_a^b x\,dx = \left.\frac{x^2}{2} \right|_a^b$$`

b. `$$\frac{dy}{dx}=y'=\lim_{h \to 0}\frac{f(x+h)-f(x)}{h}$$`

c. `\sum_n \frac{1}{n^s}=\prod_p \frac{1}{1-\frac{1}{p^s}}`

d. `$$\nabla f(x,y,z) = \left(\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z}\right)$$`

e. `$$\frac{1+\frac{a}{b}}{1+\ln{\frac{\sqrt{b^2}}{1+\frac{1}{a}}}}$$`

{{< /spoiler >}}

## Ejercicio 4

Escribir el código LaTeX para generar la siguiente expresión matricial: 

\begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1m} \newline
a_{21} & a_{22} & \dots & a_{2m} \newline
\vdots & \vdots & \ddots & \vdots \newline
a_{n1} & a_{n2} & \dots & a_{nm}
\end{bmatrix}


{{< spoiler text="Solución" >}}
```TeX
% PREÁMBULO
\usepackage{amsmath}
% CUERPO
\begin{document}
$$
\begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1m} \newline
a_{21} & a_{22} & \dots & a_{2m} \newline
\vdots & \vdots & \ddots & \vdots \newline
a_{n1} & a_{n2} & \dots & a_{nm}
\end{bmatrix}
$$
\end{document}
```

{{< /spoiler >}}