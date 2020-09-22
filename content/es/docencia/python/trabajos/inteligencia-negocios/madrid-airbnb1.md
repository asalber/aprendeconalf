---
title: Airbnb Madrid
summary: Análisis de la ocupación de alojamientos con la plataforma Airbnb en Madrid.
date: 2020
tags: [Trabajo]
categories: [Programación, Python, Inteligencia de los Negocios]
type: book
---

El objetivo de este trabajo es comprobar si se está utilizando la plataforma Airbnb por parte de empresas, en lugar de particulares, para alquiler turístico en el centro de Madrid.

### Conjunto de datos

Datos abiertos de Inside Airbnb: <a href="../datos/madrid-airbnb-listings.csv">Fichero alojamientos Madrid detallado</a>.

### Requisitos obligatorios

Sin usar Pandas:

1. Extraer del fichero de alojamientos una lista con todos los alojamientos, donde cada alojamiento sea un diccionario que contenga el identificador del alojamiento, el identificador del anfitrión, el distrito, el precio y las plazas.
2. Crear una función que reciba la lista de alojamientos y devuelva el número de alojamientos en cada distrito.
3. Crear una función que reciba la lista de alojamientos y un número de ocupantes y devuelva la lista de alojamientos con un número de plazas mayor o igual que el número de ocupantes.
4. Crear una función que reciba la lista de alojamientos un distrito, y devuelva los 10 alojamientos más baratos del distrito.
5. Crear una función que reciba la lista de alojamientos y devuelva un diccionario con los anfitriones y el número de alojamientos que posee cada uno.

Usando Pandas:

6. Preprocesar el fichero de alojamientos para crear un data frame con las variables id, host_id, listing_url, room_type, neighbourhood_group_cleansed, price, cleaning_fee, accommodates, minimum_nights, minimum_cost, review_scores_rating, latitude, longitude, is_location_exact. Eliminar del data frame cualquier fila incompleta. Añadir al data frame nuevas variables con el coste mínimo por noche y por persona (que incluya los gastos de limpieza).
7. Crear una función que reciba una lista de distritos y devuelva un diccionario con los tipos de alojamiento en ese distrito y el porcentaje de alojamientos de ese tipo.
8. Crear una función que reciba una lista de distritos y devuelva un diccionario con el número de alojamientos que cada anfitrión ofrece en esos distrito, ordenado de más a menos alojamientos.
9. Crear una función que reciba devuelva un diccionario con el número medio de alojamientos por anfitrión de cada distrito.
10. Crear una función que reciba una lista de distritos y dibuje un diagrama de sectores con los porcentajes de tipos de alojamientos en esos distritos.
11. Crear una función que dibuje un diagrama de barras con el número de alojamientos por distritos.
12. Crear una función que dibuje un diagrama de barras con los porcentajes acumulados de tipos de alojamientos por distritos.
13. Crear una función reciba una lista de distritos y una lista de tipos de alojamientos, y dibuje un diagrama de sectores con la distribución del número de alojamientos de ese tipo por anfitrión.
14. Crear una función que dibuje un diagrama de barras con los precios medios por persona y día de cada distrito.
15. Crear una función que reciba una lista de distritos y dibuje un gráfico de dispersión con el coste mínimo por noche y persona y la puntuación en esos distritos.
16. Crear una función que reciba una lista de distritos y dibuje dos histogramas con la distribución de precios por persona y día, uno para los alojamientos con título en inglés y otro para los alojamientos con títulos en español. Si la distribución es muy asimétrica, aplicar una transformación logarítmica. ¿Hay diferencias entre los precios de los alojamientos en inglés y el español? Nota: Para identificar el idioma puede usare el módulo langdetect.

## Solución

<a href="https://colab.research.google.com/github/asalber/aprendeconalf/blob/master/content/es/docencia/python/trabajos/soluciones/madrid-airbnb1.ipynb" class="btn btn-info" target="_blank">Solución</a>

Abrir con <a href="https://repl.it/@asalber/madrid-airbnb1py"><img src="/images/logo-replit.png" alt="Abrir con repl.it"></a>
