---
title: Examen de Inteligencia de los Negocios 2021-03-25
date: 2021-03-25
tags: [Exámen]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

Grado: Inteligencia de los Negocios  
Fecha: 25 de marzo de 2021

## Ejercicio 1

El cálculo del IRPF en la Hacienda española se define como progresivo. Hacienda divide los ingresos (tu renta) en tramos y asigna un porcentaje a pagar en cada uno de ellos. Estos tramos son los siguientes:

| Tramos IRPF 2021       | Tipos a aplicar |
| :--------------------- | :-------------: |
| Desde 0 hasta 12.450€  |       19%       |
| De 12.450€ a 20.200€   |       24%       |
| De 20.200€ a 35.200€   |       30%       |
| De 35.200€ en adelante |       37%       |

Por ejemplo, para una persona con una renta de 65.000€, el cálculo del impuesto se haría así:

- Primer tramo IRPF: se paga el 19% de 12.450 euros, es decir, 2.365,5 euros
- Segundo tramo IRPF: se paga el 24% de 7.750 euros (la diferencia entre el primer y segundo tramo), es decir, 1.860 euros.
- Tercer tramo IRPF: se paga el 30% de 15.000 euros (la diferencia entre el segundo y tercer tramo), es decir, 4.500 euros.
- Cuarto tramo IRPF: se paga el 37% de 29.800 euros (la diferencia entre su renta y el límite del tercer tramo), es decir, 11.026 euros.

La suma de las anteriores cantidades es el total a pagar: 19.751,5 euros.

Escribir un programa que pregunte por la renta del usuario y muestre por pantalla el IRPF que debe pagar a Hacienda.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-03-25/ejercicio1.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 2

Juan juega siempre la misma combinación a la bonoloto: 7, 13, 21, 37, 46, 49.

Construir un programa que pregunte al usuario por la combinación ganadora y diga si Juan ha ganado o, en caso contrario, muestre por pantalla la lista de los números que no ha acertado. El programa debe usar listas.

Nota: El juego de la bonoloto consiste en acertar una combinación de 6 números entre 1 y 49.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-03-25/ejercicio2.ipynb" class="btn btn-info" target="_blank">Solución</a>

## Ejercicio 3

Los productos en oferta de una tienda de informática se guardan una cadena como la de más abajo, donde cada línea (separadas por el carácter de cambio de línea ‘\n’) contiene el nombre del producto, el número de unidades en stock, el precio (en €) y el descuento que tiene (en porcentaje), separados por punto y coma.

```python
'disco duro 500Gb;200;25;15\nmemoria ram 16Gb;500;30;20\nratón inalámbrico;800;12;10\ntarjeta wifi;150;20;12'
```

Construir un programa que genere, a partir de la cadena anterior, un diccionario como el de más abajo, donde cada par corresponda un producto, siendo la clave el nombre del producto y el valor una lista con el resto de la información del producto.

```python
{‘disco duro 500Gb’: [‘200’, ‘25’, ‘15’], ‘memoria ram 16Gb’: [‘500’, ‘30’, ‘20’], ‘ratón inalámbrico’: [‘800’, ‘12’, ‘10’], ‘tarjeta wifi’: [‘150’, ‘20’, ‘12’]}
```

Después el programa debe recorrer el diccionario y mostrar por pantalla un listado con los nombres de todos los productos en oferta y su precio final tras aplicar el descuento.

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/examenes/inteligencia-negocios/soluciones/examen-2021-03-25/ejercicio3.ipynb" class="btn btn-info" target="_blank">Solución</a>
