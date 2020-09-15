---
title: Physiotherapy exam 2016-04-01
date: 2016-04-20
tags: [Exam, Statistics, Biostatistics, Physiotherapy]
categories: [Statistics, Biostatistics]
type: book
---

Grade: Physiotherapy  
Date: April 01, 2016

## Question 1
The chart below shows the cumulative frequency distribution the maximum angle of knee deflection after a replacement of the knee cap in a group of patients.

<img src="../img/knee_angle-1.svg" title="plot of chunk knee_angle" alt="plot of chunk knee_angle" style="display: block; margin: auto;" />

1. Calculate the quartiles and interpret them.
2. Are there outliers in the sample?
3. What percentage of patients have a maximum angle of knee deflection of 90 degrees?

{{< spoiler text="Solution" >}}
1. $Q_1=64$, $Q_2=83.3333$, $Q_3=100$. 
2. Fences: $F_1=10$ and $F_2=154$. There are no outliers. 
3. $F_{90}=60\%$.
{{< /spoiler >}}

## Question 2
The waiting times in a physiotherapy clinic of a sample of patiens are

<div style="text-align:center">
18, 8, 27, 6, 13, 26, 14, 23, 14, 31, 27, 19, 15, 20, 11, 30, 25, 23, 20, 15
</div>

1. Calculate the mean. Is representative? Justify the answer.
2. Calculate the coefficient of skewness and interpret it.
3. Calculate the coefficient of kurtosis and interpret it.  

Use the following sums for the calculations: $\sum x_i=385$ min, $\sum(x_i-\bar x)^2=983.75$ min$^2$, $\sum (x_i-\bar x)^3=-601.125$ min$^3$, $\sum (x_i-\bar x)^4=98369.1406$ min$^4$.




{{< spoiler text="Solution" >}}
1. $\bar x=19.25$ min, $s^2=49.1875$ min$^2$, $s=7.0134$ min, $cv=0.3643$. As the $cv<0.5$ there is a low variability and the mean is representative.
2. $g_1=-0.0871$. The distribution is almost symmetrical. 
3. $g_2=-0.9671$. The distribution is flatter than a bell curve (platykurtic).
{{< /spoiler >}}

## Question 3
A study try to determine if there is relation between recovery time $Y$ (in days) of an injury and the age of the person $X$ (in years). For that purpose a sample of 15 persons with the injury was drawn with the following values:

| Age (years) | Recovery time (days) |
|------------:|---------------------:|
|          21 |                   20 |
|          26 |                   26 |
|          30 |                   27 |
|          34 |                   32 |
|          39 |                   36 |
|          45 |                   37 |
|          51 |                   38 |
|          54 |                   41 |
|          59 |                   42 |
|          63 |                   45 |
|          71 |                   44 |
|          76 |                   43 |
|          80 |                   45 |
|          84 |                   46 |
|          88 |                   44 |

1. Compute the regression line of the recovery time on the age. How much increase the recovery time for each year of age?
2. Compute the logarithmic regression model of the recovery time on the age.
3. Which of the previous models explains better the relation between the recovery time and the age? Justify the answer.
4. Use the best of the previous models to predict the recovery time of a person 50 years old. Is reliable the prediction?

Use the following sums for the calculations:
$\sum x_i=821$, $\sum \log(x_i)=58.7255$, $\sum y_j=566$, $\sum \log(y_j)=54.0702$,
$\sum x_i^2=51703$, $\sum \log(x_i)^2=232.7697$, $\sum y_j^2=22270$, $\sum \log(y_j)^2=195.7633$,
$\sum x_iy_j=33256$, $\sum x_i\log(y_j)=3026.6478$, $\sum \log(x_i)y_j=2265.458$, $\sum \log(x_i)\log(y_j)=213.1763$.

{{< spoiler text="Solution" >}}

1. Linear model
$\bar x=54.7333$ years, $s_x^2=451.1289$ years$^2$. 
$\bar y=37.7333$ days, $s_y^2=60.8622$ days$^2$. 
$s_{xy}=151.7956$ years$\cdot$days. 
Regression line of recovery time on age: $y=19.3167 + 0.3365x$. 
Every year of age the recovery time increases 0.3365 days. 

2. Logartihmic model
$\overline{\log(x)}=3.915$ log(years), $s_{\log(x)}^2=0.1905$ log(years)$^2$. 
$s_{\log(x)y}=3.3033$ log(years)$\cdot$days. 
Logartihmic model of recovery time on age: $y=-30.1526 + 17.3398\log(x)$. 
3. Linear coefficient of determination $r^2=0.8392$. 
Logarithmic coefficient of determination $r^2=0.9411$. 
So the logarithmic model fits better. 
4. $y(50)=-30.1526 + 17.3398\log(50) = 37.6812$.
{{< /spoiler >}}
