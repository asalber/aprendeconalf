---
title: Probabilidad
summary: " " 
date: 
lastmod:
tags: [Probabilidad, Riesgos, Tests Diagnósticos]
categories: [Estadística, Bioestadística, Epidemiología]
type: book
weight: 30
---

La estadística descriptiva permite describir el comportamiento y las relaciones entre las variables en la muestra, pero no permite sacar conclusiones sobre el resto de la población.

Ha llegado el momento de dar el salto de la muestra a la población y pasar de la estadística descriptiva a la inferencia estadística, y el puente que lo permite es la **Teoría de la Probabilidad**.

Hay que tener en cuenta que el conocimiento que se puede obtener de la población a partir de la muestra es limitado, y que para obtener conclusiones válidas para la población la muestra debe ser
representativa de esta. Por esta razón, para garantizar la representatividad de la muestra, esta debe extraerse *aleatoriamente*, es decir, al *azar*.

La teoría de la probabilidad precisamente se encarga de controlar ese azar para saber hasta qué punto son fiables las conclusiones obtenidas a partir de una muestra.

## Experimentos y sucesos aleatorios

### Experimentos aleatorios

El estudio de una característica en una población se realiza a través de experimentos aleatorios.

{{% alert def %}}
**Definición - Experimento aleatorio**. Un *experimento aleatorio* es un experimento que cumple dos condiciones:

1. El conjunto de posibles resultados es conocido.
2. No se puede predecir con absoluta certeza el resultado del experimento.
{{% /alert %}}

**Ejemplo**. Un ejemplo típico de experimentos aleatorios son los juegos
de azar. El lanzamiento de un dado, por ejemplo, es un experimento
aleatorio ya que:

- Se conoce el conjunto posibles de resultados $\\\{1,2,3,4,5,6\\\}$.
- Antes de lanzar el dado, es imposible predecir con absoluta certeza el valor que saldrá.

Otro ejemplo de experimento aleatorio sería la selección de un individuo de una población al azar y la determinación de su grupo sanguíneo.

En general, la obtención de cualquier muestra mediante procedimientos aleatorios será un experimento
aleatorio.

### Espacio muestral

{{% alert def %}}
**Definición - Espacio muestral**. Al conjunto $\Omega$ de todos los posibles resultados de un
experimento aleatorio se le llama _espacio muestral_.
{{% /alert %}}

Algunos ejemplos de espacios muestrales son:

- Lanzamiento de una moneda: $\Omega=\\{c,x\\}$.
- Lanzamiento de un dado: $\Omega=\\{1,2,3,4,5,6\\}$.
- Grupo sanguíneo de un individuo seleccionado al azar:
$\Omega=\\{\mbox{A},\mbox{B},\mbox{AB},\mbox{0}\\}$.
- Estatura de un individuo seleccionado al azar:
$\Omega=\mathbb{R}^+$.

### Diagrama de árbol

En experimentos donde se mide más de una variable, la determinación del espacio muestral puede resultar compleja. En tales casos es recomendable utilizar un para construir el espacio muestral.

En un diagrama de árbol cada variable se representa en un nivel del árbol y cada posible valor de la variable como una rama.

**Ejemplo** El siguiente diagrama de árbol representa el espacio muestral de un experimento aleatorio en el que se mide el sexo y el grupo sanguineo de un individuo al azar.

<img src="../img/probabilidad/espacio_muestral.svg" alt="Diagrama de árbol del espacio muestral del sexo y el grupo sanguineo" width="500">

### Sucesos aleatorios

{{% alert def %}}
**Definición - Suceso aleatorio**. Un *suceso aleatorio* es cualquier subconjunto del espacio muestral $\Omega$ de un experimento aleatorio.
{{% /alert %}}

Existen distintos tipos de sucesos:

- **Suceso imposible**: Es el suceso vacío $\emptyset$. Este suceso nunca ocurre.
- **Sucesos elementales**: Son los sucesos formados por un solo elemento.
- **Sucesos compuestos**: Son los sucesos formados por dos o más elementos.
- **Suceso seguro**: Es el suceso que contiene el propio espacio muestral $\Omega$. Este suceso siempre ocurre.

## Teoría de conjuntos

### Espacio de sucesos

{{% alert def %}}
**Definición - Espacio de sucesos**. Dado un espacio muestral $\Omega$ de un experimento aleatorio, el conjunto formado por todos los posibles sucesos de $\Omega$ se llama *espacio de sucesos de $\Omega$* y se denota $\mathcal{P}(\Omega)$.
{{% /alert %}}

**Ejemplo**. Dado el espacio muestral $\Omega=\\{a,b,c\\}$, su espacio de sucesos es

$$\mathcal{P}(\Omega)=\left\\{\emptyset, \\{a\\},\\{b\\},\\{c\\},\\{a,b\\},\\{a,c\\},\\{b,c\\},\\{a,b,c\\}\right\\}$$

### Operaciones entre sucesos

Puesto que los sucesos son conjuntos, por medio de la teoría de
conjuntos se pueden definir las siguientes operaciones entre sucesos:

- Unión.
- Intersección.
- Complementario.
- Diferencia.

### Unión de sucesos

{{% alert def %}}
**Definición - Suceso unión**. Dados dos sucesos $A,B\subseteq \Omega$, se llama *suceso unión* de $A$ y $B$, y se denota $A\cup B$, al suceso formado por los elementos de $A$ junto a los elementos de $B$, es decir, 

$$A\cup B = \\{x\\,|\\, x\in A\textrm{ o }x\in B\\}.$$
{{% /alert %}}

<img src="../img/probabilidad/union.svg" alt="Union de dos sucesos" width="300">

El suceso unión $A\cup B$ ocurre siempre que ocurre $A$ <span style="color:red;">o</span> $B$.

### Intersección de sucesos

{{% alert def %}}
**Definición - Suceso intersección**. Dados dos sucesos $A,B\subseteq \Omega$, se llama *suceso intersección* de $A$ y $B$, y se denota $A\cap B$, al suceso formado por los elementos comunes de $A$ y $B$, es decir,

$$A\cap B = \\{x\\,|\\, x\in A\textrm{ y }x\in B\\}.$$
{{% /alert %}}

<img src="../img/probabilidad/interseccion.svg" alt="Intersección de dos sucesos" width="300">

El suceso intersección $A\cap B$ ocurre siempre que ocurren $A$ <span style="color:red;">y</span> $B$.

Diremos que dos sucesos son **incompatibles** si su intersección es vacía.

### Contrario de un suceso

{{% alert def %}}
**Definición - Suceso contrario**. Dado suceso $A\subseteq \Omega$, se llama *suceso contrario o complementario* de $A$, y se denota $\overline A$, al suceso formado por los elementos de $\Omega$ que no pertenecen a $A$, es decir,

$$\overline A = \\{x\\,|\\, x\not\in A\\}.$$
{{% /alert %}}

<img src="../img/probabilidad/contrario.svg" alt="Contrario de un suceso" width="300">

El suceso contrario $\overline A$ ocurre siempre que <span style="color:red;">no</span> ocurre $A$.

### Diferencia de sucesos

{{% alert def %}}
**Definición - Suceso diferencia**. Dados dos sucesos $A,B\subseteq \Omega$, se llama *suceso diferencia* de $A$ y $B$, y se denota $A-B$, al suceso formado por los elementos de $A$ que no pertenecen a $B$, es decir,

$$A-B = \\{x\\,|\\, x\in A\mbox{ y }x\not\in B\\} = A \cap \overline B.$$
{{% /alert %}}

<img src="../img/probabilidad/diferencia.svg" alt="Diferencia de sucesos" width="300">

El suceso diferencia $A-B$ ocurre siempre que ocurre $A$ pero no ocurre $B$, y también puede expresarse como $A\cap \bar B$.

**Ejemplo**. Dado el espacio muestral correspondiente al lanzamiento de un dado
$\Omega=\\{1,2,3,4,5,6\\}$ y los sucesos $A=\\{2,4,6\\}$ y $B=\\{1,2,3,4\\}$,

- La unión de $A$ y $B$ es $A\cup B=\\{1,2,3,4,6\\}$.
- La intersección de $A$ y $B$ es $A\cap B=\\{2,4\\}$.
- El contrario de $A$ es $\overline A=\\{1,3,5\\}$.
- Los eventos $A$ y $\overline A$ son incompatibles.
- La diferencia de $A$ y $B$ es $A-B=\\{6\\}$, y la diferencia de $B$ y $A$ es $B-A=\\{1,3\\}$.

### Álgebra de sucesos

Dados los sucesos $A,B,C\in  \mathcal{P}(\Omega)$, se cumplen las
siguientes propiedades:

1. $A\cup A=A$, $A\cap A=A$ (idempotencia).
2. $A\cup B=B\cup A$, $A\cap B = B\cap A$ (conmutativa).
3. $(A\cup B)\cup C = A\cup (B\cup C)$, $(A\cap B)\cap C = A\cap (B\cap C)$ (asociativa).
4. $(A\cup B)\cap C = (A\cap C)\cup (B\cap C)$, $(A\cap B)\cup C = (A\cup C)\cap (B\cup C)$ (distributiva).
5. $A\cup \emptyset=A$, $A\cap E=A$ (elemento neutro).
6. $A\cup E=E$, $A\cap \emptyset=\emptyset$ (elemento absorbente).
7. $A\cup \overline A = E$, $A\cap \overline A= \emptyset$ (elemento simétrico complementario).
8. $\overline{\overline A} = A$ (doble contrario).
9. $\overline{A\cup B} = \overline A\cap \overline B$, $\overline{A\cap B} = \overline A\cup \overline B$ (leyes de Morgan).
10. $A\cap B\subseteq A\cup B$.

## Definición de probabilidad

### Definición clásica de probabilidad

{{% alert def %}}
Dado un espacio muestral $\Omega$ de un experimento aleatorio donde todos los elementos de $\Omega$ son equiprobables, la *probabilidad* de un suceso $A\subseteq \Omega$ es el cociente entre el número de elementos de $A$ y el número de elementos de $\Omega$ 

$$P(A) = \frac{|A|}{|\Omega|} = \frac{\mbox{nº casos favorables a A}}{\mbox{nº casos posibles}}$$
{{% /alert %}}

Esta definición es ampliamente utilizada, aunque tiene importantes
restricciones:

  - Es necesario que todos los elementos del espacio muestral tengan la
    misma probabilidad de ocurrir (*equiprobabilidad*).

  - No puede utilizarse con espacios muestrales infinitos, o de los que
    no se conoce el número de casos posibles.

<span class="alert">*¡Ojo\! Esto no se cumple en muchos experimentos
aleatorios reales.*</span>

**Ejemplo**. Dado el espacio muestral correspondiente al lanzamiento de un dado $\Omega=\\{1,2,3,4,5,6\\}$ y el suceso $A=\\{2,4,6\\}$, la probabilidad de $A$ es

$$P(A) = \frac{|A|}{|\Omega|} = \frac{3}{6} = 0.5.$$

Sin embargo, si se considera el espacio muestral correspondiente a observar el grupo sanguíneo de un individuo al azar, $\Omega=\\{O,A,B,AB\\}$, no se puede usar la definición clásica de probabilidad para calcular la probabilidad de que tenga grupo sanguíneo $A$,

$$P(A) \neq \frac{|A|}{|\Omega|} = \frac{1}{4} = 0.25,$$

ya que los grupos sanguíneos no son igualmente probables en las poblaciones humanas.

### Definición frecuentista de probabilidad

{{% alert theo %}}
**Teorema - Ley de los grandes números**.Cuando un experimento aleatorio se repite un gran número de veces, las frecuencias relativas de los sucesos del experimento tienden a estabilizarse en torno a cierto número, que es precisamente su probabilidad.
{{% /alert %}}

De acuerdo al teorema anterior, podemos dar la siguiente definición

{{% alert def %}}
**Definición - Probabilidad frecuentista**. Dado un espacio muestral $\Omega$ de un experimento aleatorio
reproducible, la *probabilidad* de un suceso $A\subseteq \Omega$ es la frecuencia relativa del suceso $A$ en infinitas repeticiones del experimento 

$$P(A) = lim_{n\rightarrow \infty}\frac{n_{A}}{n}$$
{{% /alert %}}

Aunque esta definición es muy útil en experimentos científicos reproducibles, también tiene serios inconvenientes, ya que

  - Sólo se calcula una aproximación de la probabilidad real.
  - La repetición del experimento debe ser en las mismas condiciones.

**Ejemplo**. Dado el espacio muestral correspondiente al lanzamiento de una moneda $\Omega=\\{C,X\\}$, si después de lanzar la moneda 100 veces obtenemos 54 caras, entonces la probabilidad de $C$ es aproximadamente

$$P(C) = \frac{n_C}{n} = \frac{54}{100} = 0.54.$$

Si se considera el espacio muestral correspondiente a observar el grupo sanguíneo de un individuo al azar, $\Omega=\\{O,A,B,AB\\}$, si se toma una muestra aleatoria de 1000 personas y se observa que 412 tienen grupo sanguíneo $A$, entonces la probabilidad del grupo sanguíneo $A$ es aproximadamente

$$P(A) = \frac{n_A}{n} = \frac{412}{1000} = 0.412.$$

### Definición axiomática de probabilidad

{{% alert def %}}
**Definición - Probabilidad (Kolmogórov)**.Dado un espacio muestral $\Omega$ de un experimento aleatorio, una función de *probabilidad* es una aplicación que asocia a cada suceso $A\subseteq \Omega$ un número real $P(A)$, conocido como probabilidad de $A$, que cumple los siguientes axiomas:

1.  La probabilidad de un suceso cualquiera es positiva o nula,
    $$P(A)\geq 0.$$

2.  La probabilidad del suceso seguro es igual a la unidad,
    $$P(\Omega)=1.$$

3.  La probabilidad de la unión de dos sucesos incompatibles
    ($A\cap B=\emptyset$) es igual a la suma de las probabilidades de
    cada uno de ellos, 
    $$P(A\cup B) = P(A)+P(B).$$
{{% /alert %}}

### Consecuencias de los axiomas de probabilidad

A partir de los axiomas de la definición de probabilidad se pueden
deducir los siguientes resultados:

1.  $P(\overline A) = 1-P(A)$.
2.  $P(\emptyset)= 0$.
3.  Si $A\subseteq B$ entonces $P(A)\leq P(B)$.
4.  $P(A) \leq 1$.
5.  Si $A$ y $B$ son sucesos compatibles, es decir, su intersección no es vacía, entonces 

    $$P(A\cup B)= P(A) + P(B) - P(A\cap B).$$

6.  Si el suceso $A$ está compuesto por los sucesos elementales
    $e_1,e_2,...,e_n$, entonces 
    
    $$P(A)=\sum_{i=1}^n P(e_i).$$

{{< spoiler text="Demostración" >}}
1. $\overline A = \Omega \Rightarrow P(A\cup \overline A) = P(\Omega) \Rightarrow P(A)+P(\overline A) = 1 \Rightarrow P(\overline A)=1-P(A)$.
2. $\emptyset = \overline \Omega \Rightarrow P(\emptyset) = P(\overline \Omega) = 1-P(\Omega) = 1-1 = 0.$
3. $B = A\cup (B-A)$. Como $A$ y $B-A$ son incompatibles, $P(B) = P(A\cup (B-A)) = P(A)+P(B-A) \geq P(A).$
    
    Si pensamos en probabilidades como áreas, es fácil de ver gráficamente,
    <img src="../img/probabilidad/probabilidad_inclusion.svg" alt="Probabilidad de un suceso incluido en otro" width="300">
    
4. $A\subseteq \Omega \Rightarrow P(A)\leq P(\Omega)=1.$
5. $A=(A-B)\cup (A\cap B)$. Como $A-B$ y $A\cap B$ son incompatibles, $P(A)=P(A-B)+P(A\cap B) \Rightarrow P(A-B)=P(A)-P(A\cap B)$.
    
    Si pensamos en probabilidades como áreas, es fácil de ver gráficamente,

    <img src="../img/probabilidad/probabilidad_diferencia.svg" alt="Probabilidad de la diferencia de dos sucesos" width="300">
    
6. $A\cup B= (A-B) \cup (B-A) \cup (A\cap B)$. Como $A-B$, $B-A$ y $A\cap B$ son incompatibles, $P(A\cup
    B)=P(A-B)+P(B-A)+P(A\cap B) = P(A)-P(A\cap B)+P(B)-P(A\cap B)+P(A\cap B)= P(A)+P(B)-P(A\cup B)$.
    
    Si pensamos en probabilidades como áreas, es fácil de ver gráficamente,
    
    <img src="../img/probabilidad/probabilidad_union.svg" alt="Probabilidad de la unión de dos sucesos" width="300">

    
7. $A=\\{e_1,\cdots,e_n\\} = \\{e_1\\}\cup \cdots \cup \\{e_n\\} \Rightarrow$ $P(A)=P(\\{e_1\\}\cup \cdots \cup \\{e_n\\}) = P(\\{e_1\\})+ \cdots P(\\{e_n\\}).$
{{< /spoiler >}} 

### Interpretación de la probabilidad

Como ha quedado claro en los axiomas anteriores, la probabilidad de un evento $A$ es un número real $P(A)$ que está siempre entre 0 y 1.

En cierto modo, este número expresa la verosimilitud del evento, es decir, la confianza que hay en que ocurra $A$ en el experimento. Por tanto, también nos da una medida de la incertidumbre sobre el suceso.

- La mayor incertidumbre corresponde a $P(A)=0.5$ (Es tan probable que ocurra $A$ como que no ocurra).

- La menor incertidumbre corresponde a $P(A)=1$ ($A$ sucederá con absoluta certeza) y $P(A)=0$ ($A$ no sucederá con absoluta certeza).

Cuando $P(A)$ está más próximo a 0 que a 1, la confianza en que no ocurra $A$ es mayor que la de que ocurra $A$. Por el contrario, cuando $P(A)$ está más próximo a 1 que a 0, la confianza en que ocurra
$A$ es mayor que la de que no ocurra $A$.

## Probabilidad condicionada

### Experimentos condicionados

En algunas ocasiones, es posible que tengamos alguna información sobre el experimento antes de su realización. Habitualmente esa información se da en forma de un suceso $B$ del mismo espacio muestral que sabemos que es cierto antes de realizar el experimento.

En tal caso se dice que el suceso $B$ es un suceso *condicionante*, y la probabilidad de otro suceso $A$ se conoce como y se expresa $$P(A|B).$$

Esto debe leerse como *probabilidad de $A$ dado $B$* o *probabilidad de $A$ bajo la condición de $B$*.

Los condicionantes suelen cambiar el espacio muestral del experimento y por tanto las probabilidades de sus sucesos.

**Ejemplo**. Supongamos que tenemos una muestra de 100 hombres y 100 mujeres con las siguientes frecuencias 

$$
\begin{array}{|c|c|c|}
\hline 
 & \mbox{No fumadores} & \mbox{Fumadores} \newline
 \hline 
 \mbox{Mujeres} & 80 & 20 \newline
 \hline
 \mbox{Hombres} & 60 & 40 \newline
 \hline
\end{array}
$$ 

Entonces, usando la definición frecuentista de probabilidad, la probabilidad de que una persona elegida al azar sea fumadora es 

$$P(\mbox{Fumadora})= \frac{60}{200}=0.3.$$

Sin embargo, si se sabe que la persona elegida es mujer, entonces la muestra se reduce a la primera fila, y la probabilidad de ser fumadora es 

$$P(\mbox{Fumadora}|\mbox{Mujer})=\frac{20}{100}=0.2.$$

### Probabilidad condicionada

{{% alert def %}}
**Definición - Probabilidad condicionada**. Dado un espacio muestral $\Omega$ de un experimento aleatorio, y dos dos sucesos $A,B\subseteq \Omega$, la probabilidad de $A$ *condicionada* por $B$ es 

$$P(A|B) = \frac{P(A\cap B)}{P(B)},$$

siempre y cuando, $P(B)\neq 0$.
{{% /alert %}}

Esta definición permite calcular probabilidades sin tener que alterar el espacio muestral original del experimento.

**Ejemplo**. En el ejemplo anterior

$$P(\mbox{Fumadora}|\mbox{Mujer})= \frac{P(\mbox{Fumadora}\cap \mbox{Mujer})}{P(\mbox{Mujer})} =  \frac{20/200}{100/200}=\frac{20}{100}=0.2.$$

### Probabilidad del suceso intersección

A partir de la definición de probabilidad condicionada es posible obtener la fórmula para calcular la probabilidad de la intersección de dos sucesos. 

$$P(A\cap B) = P(A)P(B|A) = P(B)P(A|B).$$

**Ejemplo**. En una población hay un 30% de fumadores y se sabe que el 40% de los fumadores tiene cáncer de pulmón. La probabilidad de que una persona elegida al azar sea fumadora y tenga cáncer de pulmón es

$$P(\mbox{Fumadora}\cap \mbox{Cáncer})= P(\mbox{Fumadora})P(\mbox{Cáncer}|\mbox{Fumadora}) = 0.3\times 0.4 = 0.12.$$

### Independencia de sucesos

En ocasiones, la ocurrencia del suceso condicionante no cambia la
probabilidad original del suceso principal.

{{% alert def %}}
**Definición - Sucesos independientes**. Dado un espacio muestral $\Omega$ de un experimento aleatorio, dos
sucesos $A,B\subseteq \Omega$ son *independientes* si la probabilidad de $A$ no se ve alterada al condicionar por $B$, y viceversa, es decir, 

$$P(A|B) = P(A) \quad \mbox{and} \quad P(B|A)=P(B),$$ 

si $P(A)\neq 0$ y $P(B)\neq 0$.
{{% /alert %}}

Esto significa que la ocurrencia de uno evento no aporta información relevante para cambiar la incertidumbre sobre el otro.

Cuando dos eventos son independientes, la probabilidad de su intersección es igual al producto de sus probabilidades,

$$P(A\cap B) = P(A)P(B).$$

## Espacio probabilístico

{{% alert def %}}
**Definición - Espacio probabilístico**. Un *espacio probabilístico* de un experimento aleatorio es una terna $(\Omega,\mathcal{F},P)$ donde

  - $\Omega$ es el espacio muestral del experimento.
  - $\mathcal{F}$ es un un conjunto de sucesos del experimento.
  - $P$ es una función de probabilidad.
{{% /alert %}}

Si conocemos la probabilidad de todos los elementos de $\Omega$, entonces podemos calcular la  probabilidad de cualquier suceso en $\mathcal{F}$ y se puede construir fácilmente el espacio probabilístico.

### Construcción del espacio probabilístico

Para determinar la probabilidad de cada suceso elemental se puede utilizar un diagrama de árbol, mediante las siguientes reglas:

1.  Para cada nodo del árbol, etiquetar la rama que conduce hasta él con la probabilidad de que la variable en ese nivel tome el valor del nodo, condicionada por los sucesos correspondientes a sus nodos
    antecesores en el árbol.

2.  La probabilidad de cada suceso elemental en las hojas del árbol es el producto de las probabilidades de las ramas que van desde la raíz a la hoja del árbol.

<img src="../img/probabilidad/espacio_probabilistico.svg" alt="Diagrama de árbol de un espacio probabilístico" width="600">

### Árboles de probabilidad con variables dependientes

**Ejemplo**. Sea una población en la que el 30% de las personas fuman, y que la incidencia del cáncer de pulmón en fumadores es del 40% mientras que en los no fumadores es del 10%.

El espacio probabilístico del experimento aleatorio que consiste en elegir una persona al azar y medir las variables Fumar y Cáncer de pulmón se muestra a continuación.

<img src="../img/probabilidad/espacio_probabilistico_fumar_cancer.svg" alt="Diagrama de árbol del espacio probabilístico de fumar y tener cáncer de pulmón" width="550">

### Árboles de probabilidad con variables independientes

**Ejemplo** El árbol de probabilidad asociado al experimento aleatorio que consiste en el lanzamiento de dos monedas se muestra a continuación.

<img src="../img/probabilidad/espacio_probabilistico_monedas.svg" alt="Diágrama de árbol del espacio probabilístico del lanzamiento de dos monedas" width="550">

### Árboles de probabilidad con variables independientes

**Ejemplo**. Dada una población en la que hay un 40% de hombres y un 60% de mujeres, el experimento aleatorio que consiste en tomar una muestra aleatoria de tres personas tiene el árbol de probabilidad que se muestra a continuación.

<img src="../img/probabilidad/espacio_probabilistico_muestra.svg" alt="Diagrama de árbol del espacio probabilístico del sexo de tres individuos elegidos al azar" width="600">

## Teorema de la probabilidad total

### Sistema completo de sucesos

Una colección de sucesos $A_1,A_2,\ldots,A_n$ de un mismo espacio muestral $\Omega$ es un *sistema completo* si cumple las siguientes condiciones:

1.  La unión de todos es el espacio muestral:
    $A_1\cup \cdots\cup A_n =\Omega$.

2.  Son incompatibles dos a dos: $A_i\cap A_j = \emptyset$
    $\forall i\neq j$.

<img src="../img/probabilidad/particion_espacio_muestral.svg" alt="Partición del espacio muestral en un sistema completo de sucesos" width="300">

En realidad un sistema completo de sucesos es una partición del espacio muestral de acuerdo a algún atributo, como por ejemplo el sexo o el grupo sanguíneo.

### Teorema de la probabilidad total

Conocer las probabilidades de un determinado suceso en cada una de las partes de un sistema completo puede ser útil para calcular su probabilidad.

{{% alert def %}}
**Definición - Teorema de la probabilidad total**. Dado un sistema completo de sucesos $A_1,\ldots,A_n$ y un suceso $B$ de un espacio muestral $\Omega$, la probabilidad de cualquier suceso $B$ del espacio muestral se puede calcular mediante la fórmula 

$$P(B) = \sum_{i=1}^n P(A_i\cap B) = \sum_{i=1}^n P(A_i)P(B|A_i).$$
{{% /alert %}}

{{< spoiler text=Demostración >}} 
La demostración del teorema es sencilla, ya que al ser $A_1,\ldots,A_n$ un sistema completo tenemos

$$B = B\cap E = B\cap (A_1\cup \cdots \cup A_n) = (B\cap A_1)\cup \cdots \cup (B\cap A_n)$$

y como estos sucesos son incompatibles entre sí, se tiene

$$
\begin{aligned}
P(B) &= P((B\cap A_1)\cup \cdots \cup (B\cap A_n)) = P(B\cap A_1)+\cdots + P(B\cap A_n) =\newline
&= P(A_1)P(B/A_1)+\cdots + P(A_n)P(B/A_n) = \sum_{i=1}^n P(A_i)P(B/A_i).
\end{aligned}
$$

<img src="../img/probabilidad/probabilidad_total.svg" alt="Teorema de la probabilidad total" width="400">
{{< /spoiler >}}

**Ejemplo**. Un determinado síntoma $S$ puede ser originado por una enfermedad $E$ pero también lo pueden presentar las personas sin la enfermedad.
Sabemos que la prevalencia de la enfermedad $E$ es $0.2$. Además, se sabe que el $90\%$ de las personas con la enfermedad presentan el síntoma, mientras que sólo el $40\%$ de las personas sin la enfermedad lo presentan. Si se toma una persona al azar de la población, *¿qué probabilidad hay de que tenga el síntoma?*

Para responder a la pregunta se puede aplicar el teorema de la probabilidad total usando el sistema completo $\\{E,\overline{E}\\}$:

$$P(S) = P(E)P(S|E)+P(\overline E)P(S|\overline E) = 0.2\cdot 0.9 + 0.8\cdot 0.4 = 0.5.$$

Es decir, la mitad de la población tendrá el síntoma.

*¡En el fondo se trata de una media ponderada de probabilidades!*

La respuesta a la pregunta anterior es evidente a la luz del árbol de probabilidad del espacio probabilístico del experimento.

<img src="../img/probabilidad/espacio_probabilistico_total.svg" alt="Aplicación del teorema de la probabilidad total en un espacio probabilístico" width="600">

$$
\begin{aligned}
P(S) &= P(E,S) + P(\overline E,S) = P(E)P(S|E)+P(\overline E)P(S|\overline E)\newline
& = 0.2\cdot 0.9+ 0.8\cdot 0.4 = 0.18 + 0.32 = 0.5.
\end{aligned}
$$


## Teorema de Bayes

Los sucesos de un sistema completo de sucesos $A_1,\cdots,A_n$ también pueden verse como las distintas hipótesis ante un determinado hecho $B$.

En estas condiciones resulta útil poder calcular las probabilidades a posteriori $P(A_i|B)$ de cada una de las hipótesis.

{{% alert def %}}
**Definición - Teorema de Bayes**. Dado un sistema completo de sucesos $A_1,\ldots,A_n$ y un suceso $B$
de un espacio muestral $\Omega$ y otro suceso $B$ del mismo espacio muestral, la probabilidad de cada suceso $A_i$ $i=1,\ldots,n$ condicionada por $B$ puede calcularse con la siguiente fórmula

$$P(A_i|B) = \frac{P(A_i\cap B)}{P(B)} = \frac{P(A_i)P(B|A_i)}{\sum_{i=1}^n P(A_i)P(B|A_i)}.$$
{{% /alert %}}

**Ejemplo**. En el ejemplo anterior, una pregunta más interesante es qué diagnosticar a una persona que presenta el síntoma.

En este caso se puede interpretar $E$ y $\overline{E}$ como las dos posibles hipótesis para el síntoma $S$. Las probabilidades a priori para ellas son $P(E)=0.2$ y $P(\overline E)=0.8$. Esto quiere decir que si no se dispone de información sobre el síntoma, el diagnóstico será que la persona no tiene la enfermedad.

Sin embargo, si al reconocer a la persona se observa que presenta el síntoma, dicha información condiciona a las hipótesis, y para decidir entre ellas es necesario calcular sus probabilidades a posteriori, es
decir, $P(E|S)$ y P(\overline{E}|S)$.

Para calcular las probabilidades a posteriori se puede utilizar el teorema de Bayes: 

$$
\begin{aligned}
P(E|S) &= \frac{P(E)P(S|E)}{P(E)P(S|E)+P(\overline{E})P(S|\overline{E})} = \frac{0.2\cdot 0.9}{0.2\cdot 0.9 + 0.8\cdot 0.4} = \frac{0.18}{0.5}=0.36,\newline
P(\overline{E}|S) &= \frac{P(\overline{E})P(S|\overline{E})}{P(E)P(S|E)+P(\overline{E})P(S|\overline{E})} = \frac{0.8\cdot 0.4}{0.2\cdot 0.9 + 0.8\cdot 0.4} = \frac{0.32}{0.5}=0.64.
\end{aligned}
$$

Como se puede ver la probabilidad de tener la enfermedad ha aumentado.
No obstante, la probabilidad de no tener la enfermedad sigue siendo mayor que la de tenerla, y por esta razón el diagnóstico seguirá siendo que no tiene la enfermedad.

En este caso se dice que el síntoma $S$ *no es determinante* a la hora de diagnosticar la enfermedad.

## Epidemiología

Una de las ramas de la Medicina que hace un mayor uso de la probabilidad es la , que estudia la distribución y las causas de las enfermedades en las poblaciones, identificando factores de riesgos para las enfermedades de cara a la atención médica preventiva.

En Epidemiología interesa la frecuencia de un *suceso médico* $E$ (típicamente una enfermedad como la gripe, un factor de riesgo como fumar o un factor de protección como vacunarse) que se mide mediante una
variable nominal con dos categorías (ocurrencia o no del suceso).

Hay diferentes medidas relativas a la frecuencia de un suceso médico. Las más importantes son:

- Prevalencia
- Incidencia
- Riesgo relativo
- Odds ratio

### Prevalencia

{{% alert def %}}
**Definición - Prevalencia**. La *prevalencia* de un suceso médico $E$ es la proporción de una población que está afectada por el suceso.

$$\mbox{Prevalencia}(E) = \frac{\mbox{Nº individuos afectados por $E$}}{\mbox{Tamaño poblacional}}$$
{{% /alert %}}

A menudo, la prevalencia se estima mediante una muestra como la frecuencia relativa de los individuos afectados por el suceso en la muestra. Es también común expresarla esta frecuencia como un porcentaje.

**Ejemplo**. Para estimar la prevalencia de la gripe se estudió una muestra de 1000 personas de las que 150 presentaron gripe. Así, la prevalencia de la gripe es aproximadamente 150/1000=0.15, es decir, un
15%.

### Incidencia

La mide la probabilidad de ocurrencia de un suceso médico en una población durante un periodo de tiempo específico. La incidencia puede medirse como una proporción acumulada o como una tasa.

{{% alert def %}}
**Definición - Incidencia acumulada**. La *incidencia acumulada* de un suceso médico $E$ es la proporción de individuos que experimentaron el evento en un periodo de tiempo, es decir, el número de nuevos casos afectados por el evento en el periodo de tiempo, divido por el tamaño de la población inicialmente en riesgo de verse afectada.

$$R(E)=\frac{\mbox{Nº de nuevos casos con $E$}}{\mbox{Tamaño de la población en riesgo}}$$
{{% /alert %}}

**Ejemplo**. Una población contenía inicialmente $1000$ personas sin gripe y después de dos años se observó que 160 de ellas sufrieron gripe. La incidencia acumulada de la gripe es 160 casos pro 1000 personas por dos años, es decir, 16% en dos años.

### Tasa de incidencia o Riesgo absoluto

{{% alert def %}}
**Definición - Riesgo absoluto**.La *tasa de incidencia* o *riesgo absoluto* de un suceso médico $E$ es el número de nuevos casos afectados por el evento divido por la población en riesgo y por el número de unidades temporales del periodo considerado.

$$R(E)=\frac{\mbox{Nº nuevos casos con $E$}}{\mbox{Tamaño población en riesgo}\times \mbox{Nº unidades de tiempo}}$$
{{% /alert %}}

**Ejemplo**. Una población contenía inicialmente $1000$ personas sin gripe y después de dos años se observó que 160 de ellas sufrieron gripe. Si se considera el año como intervalo de tiempo, la tasa de incidencia de la gripe es 160 casos dividida por 1000 personas y por dos años, es decir, 80 casos por 1000 personas-año o 8% de personas al año.

### Prevalencia vs Incidencia

La prevalencia no debe confundirse con la incidencia. La prevalencia indica cómo de extendido está el suceso médico en una población, sin preocuparse por cuándo los sujetos se han expuesto al riesgo o durante
cuánto tiempo, mientras que la incidencia se fija en el riesgo de verse afectado por el suceso en un periodo concreto de tiempo.

Así, la prevalencia se calcula en estudios transversales en un momento temporal puntual, mientras que para medir la incidencia se necesita un estudio longitudinal que permita observar a los individuos durante un
periodo de tiempo.

La incidencia es más útil cuando se pretende entender la causalidad del suceso: por ejemplo, si la incidencia de una enfermedad en una población aumenta, seguramente hay un factor de riesgo que lo está promoviendo.

Cuando la tasa de incidencia es aproximadamente constante en la duración del suceso, la prevalencia es aproximadamente el producto de la incidencia por la duración media del suceso, es decir,

$$ \mbox{Prevalencia} = \mbox{Incidencia} \times \mbox{duración}$$

### Comparación de riesgos

Para determinar si un factor o característica está asociada con el suceso médico es necesario comparar el riesgo del suceso en dos poblaciones, una expuesta al factor y la otra no. El grupo expuesto al factor se conoce como *grupo tratamiento* o *grupo experimental* $T$ y el grupo no expuesto como *grupo control* $C$.

Habitualmente los casos observados para cada grupo se representan en una tabla de 2$\times$2 como la siguiente:

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Suceso $E$</th>
<th style="text-align: center;">No suceso $\overline E$</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Grupo tratamiento $T$</td>
<td style="text-align: center;">$a$</td>
<td style="text-align: center;">$b$</td>
</tr>
<tr class="even">
<td style="text-align: left;">Grupo control $C$</td>
<td style="text-align: center;">$c$</td>
<td style="text-align: center;">$d$</td>
</tr>
</tbody>
</table>

### Riesgo atribuible o diferencia de riesgos $RA$

{{% alert def %}}
**Definición - Riesgo atribuible**. El *riesgo atribuible* o *diferencia de riesgo* de un suceso médico
$E$ para los individuos expuestos a un factor es la diferencia entre los riesgos absolutos de los grupos tratamiento y control.

$$RA(E)=R_T(E)-R_C(E)=\frac{a}{a+b}-\frac{c}{c+d}.$$
{{% /alert %}}

El riesgo atribuible es el riesgo de un suceso que es debido específicamente al factor de interés.

Obsérvese que el riesgo atribuible puede ser positivo, cuando el riesgo del grupo tratamiento es mayor que el del grupo control, o negativo, de lo contrario.

**Ejemplo**. Para determinar la efectividad de una vacuna contra la gripe, una muestra de 1000 personas sin gripe fueron seleccionadas al comienzo del año. La mitad de ellas fueron vacunadas (grupo tratamiento) y la otra mitad recibieron un placebo (grupo control). La tabla siguiente resume los resultados al final del año.

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Gripe $E$</th>
<th style="text-align: center;">No gripe $\overline E$</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Grupo tratamiento (vacunados)</td>
<td style="text-align: center;">20</td>
<td style="text-align: center;">480</td>
</tr>
<tr class="even">
<td style="text-align: left;">Grupo control (No vacunados)</td>
<td style="text-align: center;">80</td>
<td style="text-align: center;">420</td>
</tr>
</tbody>
</table>

El riesgo atribuible de contraer la gripe cuando se es vacunado es 

$$AR(D) = \frac{20}{20+480}-\frac{80}{80+420} = -0.12.$$ 

Esto quiere decir que el riesgo de contraer la gripe es un 12% menor en vacunados
que en no vacunados.

### Riesgo relativo $RR$

{{% alert def %}}
**Definición - Teorema de Bayes**. El *riesgo relativo* de un suceso médico $E$ para los individuos expuestos a un factor es el cociente entre las proporciones de individuos afectados por el suceso en un periodo de tiempo de los grupos tratamiento y control. Es decir, el cociente entre las incidencias de
grupo tratamiento y el grupo control.

$$RR(D)=\frac{\mbox{Riesgo grupo tratamiento}}{\mbox{Riesgo grupo control}}=\frac{R_T(E)}{R_C(E)}=\frac{a/(a+b)}{c/(c+d)}$$
{{% /alert %}}

El riesgo relativo compara el riesgo de desarrollar un suceso médico entre el grupo tratamiento y el grupo control.

- $RR=1$ $\Rightarrow$ No hay asociación entre el suceso y la exposición al factor.
- $RR<1$ $\Rightarrow$ La exposición al factor disminuye el riesgo del suceso.
- $RR>1$ $\Rightarrow$ La exposición al factor aumenta el riesgo del suceso.

Cuanto más lejos de 1, más fuerte es la asociación.

**Ejemplo**. Para determinar la efectividad de una vacuna contra la gripe, una muestra de 1000 personas sin gripe fueron seleccionadas al comienzo del año. La mitad de ellas fueron vacunadas (grupo tratamiento) y la otra mitad recibieron un placebo (grupo control). La tabla siguiente resume los resultados al final del año.

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Gripe $E$</th>
<th style="text-align: center;">No gripe $\overline E$</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Grupo tratamiento (vacunados)</td>
<td style="text-align: center;">20</td>
<td style="text-align: center;">480</td>
</tr>
<tr class="even">
<td style="text-align: left;">Grupo control (No vacunados)</td>
<td style="text-align: center;">80</td>
<td style="text-align: center;">420</td>
</tr>
</tbody>
</table>

El riesgo relativo de contraer la gripe cuando se es vacunado es 

$$RR(D) = \frac{20/(20+480)}{80/(80+420)} = 0.25.$$

Así, la probabilidad de contraer la gripe en los individuos vacunados fue la cuarta parte de
la de contraerla en el caso de no haberse vacunado, es decir, la vacuna reduce el riesgo de gripe un 75%.

### Odds

Una forma alternativa de medir el riesgo de un suceso médico es el *odds*.

El *odds* de un suceso médico $E$ en una población es el cociente entre el número de individuos que adquirieron el suceso y los que no en un periodo de tiempo.

$$ODDS(E)=\frac{\mbox{Nº nuevos casos con $E$}}{\mbox{Nº casos sin $E$}}=\frac{P(E)}{P(\overline E)}$$

A diferencia de la incidencia, que es una proporción menor o igual que 1, el odds puede ser mayor que 1. No obstante es posible convertir el odds en una probabilidad con al fórmula 

$$P(E) = \frac{ODDS(E)}{ODDS(E)+1}$$

**Ejemplo** Una población contenía inicialmente $1000$ personas sin gripe. Después de un año 160 de ellas tuvieron gripe. Entonces el odds de la gripe es 160/840.

Obsérvese que la incidencia es 160/1000.

### Odds ratio $OR$ 

{{% alert def %}}
**Definición - Odds ratio**. El *odds ratio* o la *oportunidad relativa* de un suceso médico $E$
para los individuos expuestos a un factor es el cociente entre los odds del sucesos de los grupos tratamiento y control.

$$OR(E)=\frac{\mbox{Odds en grupo tratamiento}}{\mbox{Odds en grupo control}}=\frac{a/b}{c/d}=\frac{ad}{bc}$$
{{% /alert %}}

El odds ratio compara los odds de un suceso médico entre el grupo tratamiento y control. La interpretación es similar a la del riesgo relativo:

- $OR=1$ $\Rightarrow$ No existe asociación entre el suceso y la exposición al factor.
- $OR<1$ $\Rightarrow$ La exposición al factor disminuye el riesgo del suceso.
- $OR>1$ $\Rightarrow$ La exposición al factor aumenta el riesgo del suceso.

Cuanto más lejos de 1, más fuerte es la asociación.

**Ejemplo**. Para determinar la efectividad de una vacuna contra la gripe, una muestra de 1000 personas sin gripe fueron seleccionadas al comienzo del año. La mitad de ellas fueron vacunadas (grupo tratamiento) y la otra mitad recibieron un placebo (grupo control). La tabla siguiente resume los resultados al final del año.

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Gripe $E$</th>
<th style="text-align: center;">No gripe $\overline E$</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Grupo tratamiento (vacunados)</td>
<td style="text-align: center;">20</td>
<td style="text-align: center;">480</td>
</tr>
<tr class="even">
<td style="text-align: left;">Grupo control (No vacunados)</td>
<td style="text-align: center;">80</td>
<td style="text-align: center;">420</td>
</tr>
</tbody>
</table>

El odds ratio de sufrir la gripe para los individuos vacunados es 

$$OR(D) = \frac{20/480}{80/420} = 0.21875.$$ 

Esto quiere decir que el odds de sufrir la gripe frente a no sufrirla en los vacunados es casi un quinto del de los no vacunados, es decir, que aproximadamente por cada 22 personas vacunadas con gripe habrá 100 personas no vacunadas con gripe.

### Riesgo relativo vs Odds ratio

El riesgo relativo y el odds ratio son dos medidas de asociación pero su interpretación es ligeramente diferente. Mientras que el riesgo relativo expresa una comparación de riesgos entre los grupos tratamiento y control, el odds ratio expresa una comparación de odds, que no es lo mismo que el riesgo. Así, un odds ratio de 2 *no* significa que el grupo tratamiento tiene el doble de riesgo de adquirir el suceso.

La interpretación del odds ratio es un poco más enrevesada porque es contrafactual, y nos da cuántas veces es más frecuente el suceso en el grupo tratamiento en comparación con el control, asumiendo que en el
grupo control es tan frecuente que ocurra el suceso como que no.

La ventaja del odds ratio es que no depende de la prevalencia o la incidencia del suceso, y debe usarse siempre que el número de individuos que presenta el suceso se selecciona arbitrariamente en ambos grupos,
como ocurre en los estudios casos-control.

**Ejemplo**. Para determinar la asociación entre el cáncer de pulmón y fumar se tomaron dos muestras (la segunda con el doble de individuos sin cáncer) obteniendo los siguientes resultados:

**Sample 1**

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Cáncer</th>
<th style="text-align: center;">No cáncer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Fumadores</td>
<td style="text-align: center;">60</td>
<td style="text-align: center;">80</td>
</tr>
<tr class="even">
<td style="text-align: left;">No fumadores</td>
<td style="text-align: center;">40</td>
<td style="text-align: center;">320</td>
</tr>
</tbody>
</table>

$$
\begin{aligned}
RR(D) &= \frac{60/(60+80)}{40/(40+320)} = 3.86.\newline
OR(D) &= \frac{60/80}{40/320} = 6. 
\end{aligned}
$$

**Sample 2**

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Cáncer</th>
<th style="text-align: center;">No cáncer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Fumadores</td>
<td style="text-align: center;">60</td>
<td style="text-align: center;">160</td>
</tr>
<tr class="even">
<td style="text-align: left;">No fumadores</td>
<td style="text-align: center;">40</td>
<td style="text-align: center;">640</td>
</tr>
</tbody>
</table>

$$
\begin{aligned}
RR(D) &= \frac{60/(60+160)}{40/(40+640)} = 4.64.\newline
OR(D) &= \frac{60/160}{40/640} = 6. 
\end{aligned}
$$

Así, cuando cambia la incidencia o prevalencia de un suceso (cáncer de pulmón) el riesgo relativo cambia, mientras que el odds ratio no.

### Riesgo relativo vs Odds ratio

La relación entre el riesgo relativo y el odds ratio viene dada por la siguiente fórmula

$$RR = \frac{OR}{1-R_0+R_0\cdot OR} = OR \frac{1-R_1}{1-R_0},$$

donde $R_C$ and $R_T$ son la prevalencia o la incidencia en los grupos control y tratamiento respectivamente.

El odds ratio siempre sobrestima el riesgo relativo cuando este es mayor que 1 y lo subestima cuando es menor que 1. No obstante, con sucesos médicos raros (con una prevalencia o incidencia baja) el riesgo
relativo y el odds ratio son casi iguales.

<img src="../img/probabilidad/odds_ratio_vs_riesgo_relativo.svg" alt="Odss ratio versus riesgo relativo" width="600">

## Tests diagnósticos

En Epidemiología es común el uso de test para diagnosticar enfermedades.

Generalmente estos test no son totalmente fiables, sino que hay cierta probabilidad de acierto o fallo en el diagnóstico, que suele representarse en la siguiente tabla:

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Presencia enfermedad $E$</th>
<th style="text-align: center;">Ausencia enfermedad $\overline E$</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Test positivo $+$</td>
<td style="text-align: center;"><span style="color: green">Verdadero positivo </span>$VP$</td>
<td style="text-align: center;"><span style="color: red">Falso positivo </span>$FP$</td>
</tr>
<tr class="even">
<td style="text-align: left;">Test negativo $−$</td>
<td style="text-align: left;"><span style="color: red">Falso negativo </span>$FN$</td>
<td style="text-align: left;"><span style="color: green">Verdadero Negativo </span>$VN$</td>
</tr>
</tbody>
</table>

### Sensibilidad y especificidad de un test diagnóstico

La fiabilidad de un test diagnóstico depende de las siguientes probabilidades.

{{% alert def %}}
**Definición - Sensibilidad**. La *sensibilidad* de un test diagnóstico es la proporción de resultados positivos del test en personas con la enfermedad, 

$$P(+|E)=\frac{VP}{VP+FN}$$
{{% /alert %}}

{{% alert def %}}
**Definición - Especificidad**. La *especificidad* de un test diagnóstico es la proporción de resultados
negativos del test en personas sin la enfermedad,

$$P(-|\overline{E})=\frac{VN}{VN+FP}$$
{{% /alert %}}

Normalmente existe un balance entre la sensibilidad y la especificidad.

Un test con una alta sensibilidad detectará la enfermedad en la mayoría de las personas enfermas, pero también dará más falsos positivos que un test menos sensible. De este modo, un resultado positivo en un test con una gran sensibilidad no es muy útil para confirmar la enfermedad, pero un resultado negativo es útil para descartar la enfermedad, ya que raramente da resultados negativos en personas con la enfermedad.

Por otro lado, un test con una alta especificidad descartará la enfermedad en la mayoría de las personas sin la enfermedad, pero también producirá más falsos negativos que un test menos específico. Así, un
resultado negativo en un test con una gran especificidad no es útil para descartar la enfermedad, pero un resultado positivo es muy útil para confirmar la enfermedad, ya que raramente da resultados positivos en
personas sin la enfermedad.

Decidir entre un test con una gran sensibilidad o un test con una gran especificidad depende del tipo de enfermedad y el objetivo del test. En general, utilizaremos un test sensible cuando:

- La enfermedad es grave y es importante detectarla.
- La enfermedad es curable.
- Los falsos positivos no provocan traumas serios.

Y utilizaremos un test específico cuando:

- La enfermedad es importante pero difícil o imposible de curar.
- Los falsos positivos pueden provocar traumas serios.
- El tratamiento de los falsos positivos puede tener graves consecuencias.

### Valores predictivos de un test diagnóstico

Pero el aspecto más importante de un test diagnóstico es su poder predictivo, que se mide con las siguientes probabilidades a posteriori.

{{% alert def %}}
**Definición - Valor predictivo positivo**. El *valor predictivo positivo* de un test diagnóstico es la proporción de personas con la enfermedad entre las personas con resultado positivo
en el test, 

$$P(E|+) = \frac{VP}{VP+FP}$$

{{% /alert %}}

{{% alert def %}}
**Definición - Valor predictivo negativo**. El *valor predictivo negativo* de un test diagnóstico es la proporción de personas sin la enfermedad entre las personas con resultado negativo en el test, 

$$P(\overline{E}|-) = \frac{VN}{VN+FN}$$

{{% /alert %}}

Los valores predictivos positivo y negativo permiten confirmar o descartar la enfermedad, respectivamente, si alcanzan al menos el umbral de $0.5$. 

$$
\begin{array}{rcl}
VPP>0.5 & \Rightarrow & \mbox{Diagnosticar la enfermedad}\newline
VPN>0.5 & \Rightarrow & \mbox{Diagnosticar la no enfermedad} 
\end{array}
$$

No obstante, estas probabilidades dependen de la proporción de personas con la enfermedad en la población $P(E)$ que se conoce como de la enfermedad. Pueden calcularse a partir de la sensibilidad y la especificidad del test diagnóstico usando el teorema de Bayes.

$$
\begin{aligned}
VPP=P(E|+) &= \frac{P(E)P(+|E)}{P(E)P(+|E)+P(\overline{E})P(+|\overline{E})}\newline
VPN=P(\overline{E}|-) &= \frac{P(\overline{E})P(-|\overline{E})}{P(E)P(-|E)+P(\overline{E})P(-|\overline{E})}
\end{aligned}
$$

Así, con enfermedades frecuentes, el valor predictivo positivo aumenta, y con enfermedades raras, el valor predictivo negativo aumenta.

**Ejemplo** Un test diagnóstico para la gripe se ha aplicado a una muestra aleatoria de 1000 personas. Los resultados aparecen resumidos en la siguiente
tabla.

<table>
<thead>
<tr class="header">
<th style="text-align: left;"></th>
<th style="text-align: center;">Presencia de gripe $E$</th>
<th style="text-align: center;">Ausencia de gripe $\overline E$</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Test $+$</td>
<td style="text-align: center;">95</td>
<td style="text-align: center;">90</td>
</tr>
<tr class="even">
<td style="text-align: left;">Test $−$</td>
<td style="text-align: center;">5</td>
<td style="text-align: center;">810</td>
</tr>
</tbody>
</table>

Según esta muestra, la prevalencia de la gripe puede estimarse como

$$P(E) = \frac{95+5}{1000} = 0.1.$$

La sensibilidad del test diagnóstico es

$$P(+|E) = \frac{95}{95+5}= 0.95.$$

Y la especificidad es 

$$P(-|\overline{E}) = \frac{810}{90+810}=0.9.$$


El valor predictivo positivo del test es 

$$VPP = P(E|+) = \frac{95}{95+90} = 0.5135.$$

Como este valor es mayor que $0.5$, eso significa que se diagnosticará la gripe si el resultado del test es positivo. No obstante, la confianza en el diagnóstico será baja, ya que el valor es poco mayor que $0.5$.

Por otro lado, el valor predictivo negativo es 

$$VPN = P(\overline{E}|-) = \frac{810}{5+810} = 0.9939.$$

Como este valor es casi 1, eso significa que es casi seguro que no se tiene la gripe cuando el resultado del test es negativo.

Así, se puede concluir que este test es muy potente para descartar la gripe, pero no lo est tanto para confirmarla.

### Razón de verosimilitud de un test diagnóstico

La siguientes medidas también se derivan de la sensibilidad y la especificidad de un test diagnóstico.

{{% alert def %}}
**Definición - Razón de verosimilitud positiva**. La *razón de verosimilitud positiva* de un test diagnóstico es el cociente entre la probabilidad de un resultado positivo en personas con
la enfermedad y personas sin la enfermedad, respectivamente.

$$RV+=\frac{P(+|E)}{P(+|\overline{E})} = \frac{\mbox{Sensibilidad}}{1-\mbox{Especificidad}}$$

{{% /alert %}}

{{% alert def %}}
**Definición - Razón de verosimilitud negativa**. La *razón de verosimilitud negativa* de un test diagnóstico es el cociente entre la probabilidad de un resultado negativo en personas con la enfermedad y personas sin la enfermedad, respectivamente.

$$RV-=\frac{P(-|E)}{P(-|\overline{E})} = \frac{1-\mbox{Sensibilidad}}{\mbox{Especificidad}}$$

{{% /alert %}}

La razón de verosimilitud positiva puede interpretarse como el número de veces que un resultado positivo es más probable en personas con la enfermedad que en personas sin la enfermedad.

Por otro lado, la razón de verosimilitud negativa puede interpretarse como el número de veces que un resultado negativo es más probable en personas con la enfermedad que en personas sin la enfermedad.

Las probabilidades a posteriori pueden calculares a partir de las probabilidades a priori usando las razones de verosimilitud

$$P(E|+) = \frac{P(E)P(+|E)}{P(E)P(+|E)+P(\overline{E})P(+|\overline{E})} = \frac{P(E)RV+}{1-P(E)+P(E)RV+}$$

Así,

- Una razón de verosimilitud positiva mayor que 1 aumenta la probabilidad de la enfermedad.
- Una razón de verosimilitud positiva menor que 1 disminuye la probabilidad de la enfermedad.
- Una razón de verosimilitud 1 no cambia la probabilidad a priori de la de tener la enfermedad.
 
<img src="../img/probabilidad/razon_verosimilitud.svg" alt="Razón de verosimilitud" width="600">
