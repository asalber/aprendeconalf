---
title: Problems of Frequency Tables and Charts
linkTitle: Frequency Tables and Charts
date: 
lastmod:
tags: [Frequencies, Charts]
categories: [Statistics, Biostatistics]
type: book
weight: 10
---

## Exercise 1

Classify the following variables

1. Daily hours of exercise.
2. Nationality.
3. Blood pressure.
4. Severity of illness.
5. Number of sport injuries in a year.
6. Daily calorie intake.
7. Size of clothing.
8. Subjects passed in a course.

{{< spoiler text="Solution" >}}

1. Quantitative continuous.
2. Qualitative nominal.
3. Quantitative continuous.
4. Qualitative ordinal.
5. Quantitative discrete.
6. Quantitative continuous.
7. Qualitative ordinal.
8. Quantitative discrete.
{{< /spoiler >}}

## Exercise 2

The number of injuries suffered by the members of a soccer team in a league were

```
0 1 2 1 3 0 1 0 1 2 0 1 1 1 2 0 1 3 2 1 2 1 0 1
```

Compute:

1. Construct the frequency distribution table of the sample.
2. Draw the bar chart of the sample and the polygon.
3. Draw the cumulative frequency bar chart and polygon.

{{< spoiler text="Solution" >}}

| Injuries | $n_i$ |  $f_i$ | $N_i$ |  $F_i$ |
| :------- | ----: | -----: | ----: | -----: |
| 0        |     6 | 0.2500 |     6 | 0.2500 |
| 1        |    11 | 0.4583 |    17 | 0.7083 |
| 2        |     5 | 0.2083 |    22 | 0.9167 |
| 3        |     2 | 0.0833 |    24 | 1.0000 |

2.
<img src="../img/injuries_soccer_team_barchart-1.svg" title="plot of chunk injuries_soccer_team_barchart" alt="plot of chunk injuries_soccer_team_barchart" style="display: block; margin: auto;" />
3. 
<img src="../img/injuries_soccer_team_cumulative_barchart-1.svg" title="plot of chunk injuries_soccer_team_cumulative_barchart" alt="plot of chunk injuries_soccer_team_cumulative_barchart" style="display: block; margin: auto;" />
{{< /spoiler >}}

## Exercise 3

A survey about the daily number of medicines consumed by people over 70 shows the following results:

```
3 1 2 2 0 1 4 2 3 5 1 3 2 3 1 4 2 4 3 2 3 5 0 1 2 0 2 3 0 1 1 5 3 4 2 3 0 1 2 3
```

1. Construct the frequency distribution table of the sample.
2. Draw the bar chart of the sample and the polygon.
3. Draw the cumulative relative frequency bar chart and polygon.

{{< spoiler text="Solution" >}}
1. 
| Medicines | $n_i$ | $f_i$ | $N_i$ | $F_i$ |
| :-------- | ----: | ----: | ----: | ----: |
| 1         |     8 | 0.200 |    13 | 0.325 |
| 2         |    10 | 0.250 |    23 | 0.575 |
| 3         |    10 | 0.250 |    33 | 0.825 |
| 4         |     4 | 0.100 |    37 | 0.925 |
| 5         |     3 | 0.075 |    40 | 1.000 |

2.
<img src="../img/medicines_people_over_70_barchart-1.svg" title="plot of chunk medicines_people_over_70_barchart" alt="plot of chunk medicines_people_over_70_barchart" style="display: block; margin: auto;" />
3. 
<img src="../img/medicines_people_over_70_cumulative_relative_barchart-1.svg" title="plot of chunk medicines_people_over_70_cumulative_relative_barchart" alt="plot of chunk medicines_people_over_70_cumulative_relative_barchart" style="display: block; margin: auto;" />
  {{< /spoiler >}}

## Exercise 4

In a survey about the dependency of older people, 23 persons over 75 years were asked about the help they need in daily life. The answers were

```
B D A B C C B C D E A B C E A B C D B B A A B
```

where the meanings of letters are:

A No help.
B Help climbing stairs.
C Help climbing stairs and getting up from a chair or bed.
D Help climbing stairs, getting up and dressing.
E Help for almost everything.

Construct the frequency distribution table and a suitable chart.

{{< spoiler text="Solution" >}}
| Help | $n_i$ |  $f_i$ | $N_i$ |  $F_i$ |
| :--- | ----: | -----: | ----: | -----: |
| A    |     5 | 0.2174 |     5 | 0.2174 |
| B    |     8 | 0.3478 |    13 | 0.5652 |
| C    |     5 | 0.2174 |    18 | 0.7826 |
| D    |     3 | 0.1304 |    21 | 0.9130 |
| E    |     2 | 0.0870 |    23 | 1.0000 |

<img src="../img/help_daily_life_piechart-1.svg" title="plot of chunk help_daily_life_piechart" alt="plot of chunk help_daily_life_piechart" style="display: block; margin: auto;" />
{{< /spoiler >}}

## Exercise 5
The number of people treated in the emergency service of a hospital every day of November was

```
15 23 12 10 28 7 12 17 20 21 18 13 11 12 26 30 6 16 19 22 14 17 21 28 9 16 13 11 16 20
```

1. Construct the frequency distribution table of the sample.
2. Draw a suitable chart for the frequency distribution.
3. Draw a suitable chart for the cumulative frequency distribution.

{{< spoiler text="Solution" >}}
1. 
| People  | $n_i$ |  $f_i$ | $N_i$ |  $F_i$ |
| :------ | ----: | -----: | ----: | -----: |
| [5,10]  |     4 | 0.1333 |     4 | 0.1333 |
| (10,15] |     9 | 0.3000 |    13 | 0.4333 |
| (15,20] |     9 | 0.3000 |    22 | 0.7333 |
| (20,25] |     4 | 0.1333 |    26 | 0.8667 |
| (25,30] |     4 | 0.1333 |    30 | 1.0000 |

1. 
<img src="../img/people_treated_emergency_service_histogram-1.svg" title="plot of chunk people_treated_emergency_service_histogram" alt="plot of chunk people_treated_emergency_service_histogram" style="display: block; margin: auto;" />
3. 
<img src="../img/people_treated_emergency_service_cumulative_histogram-1.svg" title="plot of chunk people_treated_emergency_service_cumulative_histogram" alt="plot of chunk people_treated_emergency_service_cumulative_histogram" style="display: block; margin: auto;" />
{{< /spoiler >}}

## Exercise 6
The following frequency distribution table represents the distribution of time (in min) required by people attended in a medical dispensary.

$$
\begin{array}{|c|c|c|c|c|}
\hline \mbox{Time} & n_{i} & f_{i} & N_{i} & F_{i}\newline
\hline
\left[ 0,5\right) & 2 &  &  &  \newline
\hline
\left[ 5,10\right) &  &  & 8 &  \newline
\hline
\left[ 10,15\right) &  & &  & 0.7 \newline
\hline
\left[ 15,20\right) & 6 &  &  &\newline
\hline
\end{array}
$$

1. Complete the table.
2. Draw the ogive.

{{< spoiler text="Solution" >}}
1.
$$
\begin{array}{|c|c|c|c|c|}
\hline \mbox{Time} & n_{i} & f_{i} & N_{i} & F_{i}\newline
\hline
\left[ 0,5\right) & 2 & 0.1 & 2 & 0.1 \newline
\hline
\left[ 5,10\right) & 6 & 0.3 & 8 & 0.4 \newline
\hline
\left[ 10,15\right) & 6 & 0.3 & 14 & 0.7 \newline
\hline
\left[ 15,20\right) & 6 & 0.3 & 20  & 1\newline
\hline
\end{array}
$$

2. 
<img src="../img/time_medical_dispensary_ogive-1.svg" title="plot of chunk time_medical_dispensary_ogive" alt="plot of chunk time_medical_dispensary_ogive" style="display: block; margin: auto;" />
{{< /spoiler >}}

## Exercise 7

The following table represents the frequency distribution of the yearly uses of a health insurance in a sample of clients of a insurance company.

| uses | clients |
| ---: | ------: |
|    0 |       4 |
|    1 |       8 |
|    2 |       6 |
|    3 |       3 |
|    4 |       2 |
|    5 |       1 |
|    7 |       1 |

Draw the box plot. Study the symmetry of the distribution.

{{< spoiler text="Solution" >}}
<img src="../img/boxplot_uses_health_insurance-1.svg" title="plot of chunk boxplot_uses_health_insurance" alt="plot of chunk boxplot_uses_health_insurance" style="display: block; margin: auto;" />
{{< /spoiler >}}

## Exercise 8

The box plots below correspond to the age of a sample of people by marital status.

<img src="../img/ages_marital_status_boxplot-1.svg" title="plot of chunk ages_marital_status_boxplot" alt="plot of chunk ages_marital_status_boxplot" style="display: block; margin: auto;" />

1. Which group has higher ages?
2. Which group has lower central dispersion?
3. Which groups have outliers?
4. At which group is the age distribution more asymmetric?

{{< spoiler text="Solution" >}}
1. Widowers.
2. Divorced.
3. Widowers and divorced.
4. Divorced.
{{< /spoiler >}}
