---
title: Deuda Pública
summary: Análisis de la deuda pública por Países y tipologías.
date: 2020
tags: [Trabajo]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

El objetivo de este trabajo es hacer un análisis del endeudamiento público por países.

## Conjunto de datos

Datos del banco mundial: [Deuda pública países](datos/deuda-publica.csv) y [PIB países](datos/pib.csv).

## Requisitos

Sin usar la librería Pandas:

1. Crear una función que reciba un país y un tipo de deuda y devuelva un diccionario con todos los periodos y la cantidad de deuda en esos periodos de ese país y tipo de deuda.
2. Crear una función que reciba un país y un tipo de deuda y devuelva un diccionario con el mínimo y el máximo de deuda de ese tipo para ese país.
3. Crear una función que reciba un país y un año, y devuelva un diccionario con la deuda interna y la deuda externa de ese país en ese año.
4. Crear una función que reciba un país y un año, y devuelva un diccionario con la deuda en moneda local y la deuda en moneda extranjera de ese país en ese año.

Usando Pandas:

5. Preprocesar el fichero de deuda pública para obtener un data frame con el país, el tipo de deuda, la fecha y la cantidad de deuda.
6. Crear una función que reciba un país y una fecha y devuelva un diccionario con la deuda total interna, externa, en moneda local, en moneda extranjera, a corto plazo y a largo plazo, de ese país en esa fecha.
7. Crear una función que reciba un tipo de deuda y una fecha, y devuelva un diccionario con la deuda de ese tipo de todos los países en esa fecha.
8. Crear una función que reciba un país y una fecha y dibuje un diagrama de sectores con la deuda interna y la deuda externa de ese país en esa fecha.
9. Crear una función que reciba un país y una fecha, y dibuje un diagrama de barras con las cantidades de los distintos tipos de deudas de ese país en esa fecha.
10. Crear una función que reciba una lista de países y un tipo de deuda y dibuje un diagrama de líneas con la evolución de ese tipo de deuda de esos países (una línea por país).
11. Crear una función que reciba un país y una lista de tipos de deuda y dibuje un diagrama de líneas con la evolución de esos tipos de deuda de ese país (una línea por tipo de deuda).
12. Crear una función que reciba una lista de países y una lista de tipos de deuda, y dibuje un diagrama de cajas con las deudas de esos tipos de esos países (una caja por país y tipo de deuda).
13. Preprocesar el fichero del PIB crear un data frame con el país, la fecha y el PIB.
14. Crear una función que reciba un país y dibuje la evolución de la deuda pública total como porcentaje del PIB.
15. Crear una función que reciba un país devuelva un diccionario con los años y si el endeudamiento en esa fecha era insostenible. Se considera un endeudamiento insostenible si durante los tres años anteriores el porcentaje de deuda pública con respecto al PIB es superior al 20%.

## Solución

<a href="https://colab.research.google.com/github/asalber/asalber.github.io/blob/master/python/trabajos/soluciones/deuda-publica.ipynb" class="btn btn-info" target="_blank">Solución</a>

Abrir con <a href="https://repl.it/@asalber/deudapy"><img src="/images/logo-replit.png" alt="Abrir con repl.it"></a>