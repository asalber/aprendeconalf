---
title: Physiotherapy exam 2017-03-31
date: 2017-03-31
tags: [Exam, Statistics, Biostatistics]
categories: [Statistics, Biostatistics, Physiotherapy, Medicine]
type: book
---

Degrees: Physiotherapy, Medicine  
Date: March 31, 2017

## Question 1

The table below gives the distribution of points obtained by students in a physiotherapy public competition this year.

$$
\begin{array}{|c|r|r|r|r|r|}
\hline
x & n_i & x_in_i & x_i^2n_i & (x_i-\bar x)^3n_i & (x_i-\bar x)^4n_i\newline
\hline
(0,40] & 84 & 1680 & 33600 & -12155062.50 & 638140781.25\newline
(40,80] & 185 & 11100 & 666000 & -361328.13 & 4516601.56\newline
(80,120] & 72 & 7200 & 720000 & 1497375.00 & 41177812.50\newline
(120,160] & 40 & 5600 & 784000 & 12301875.00 & 830376562.50\newline
(160,200] & 19 & 3420 & 615600 & 23603640.63 & 2537391367.19\newline
\hline
\sum & 400 & 29000 & 2819200 & 24886500.00 & 4051603125.00\newline
\hline
\end{array}
$$

1. Compute the interquartile range and explain your result. Are there outliers in the sample?
2. The minimum number of points to pass the exam is 150; what percentage of students passed the exam?
3. If the mean of the score of the previous year exam was 80 points and the standard deviation was 52 points, which year is the mean more representative? Justify the answer.
4. According to the values of skewness and kurtosis, can we assume that the sample has been taken from a normally distributed population?
5. What score is relatively higher, 150 points in this year exam or 160 in the previous year exam? Justify the answer.



{{< spoiler text="Solution" >}}
1. $Q_1=43.48$ points, $Q_3=97.78$ points and $IQR=54.3$ points.
Fences: $F_1=-37.97$ points and $F_2=179.23$ points. Thus, there are outliers. 
2. $F_{150}=0.925$, so the percentage of students that passed the exam is $7.5\%$. 
3. This year: $\bar x=72.5$ points, $s^2=1791.75$ points², $s=42.3291$ points, $cv=0.5838$. 
Previous year: $\bar x=80$ points, $s=52$ points, $cv=0.65$. 
As the coefficient of variation of this year is less than the one of the previous year, there is less relative spread this year and the mean is more representative. 
4. $g_1=0.8203$, so the distribution is right-skewed. $g_2=0.1551$, so the distribution is a little bit more peaked than a bell curve (leptokurtic). As $g_1$ and $g_2$ are between -2 and 2 we can assume that the sample has been taken from a normaly distributed population. 
5. This year standard score: $z(150)=1.83$.
Previous year standard score: $z(160)=1.53$.
As the standard score of 150 this year is greater than the standard score of 160 the previous year, 150 points this year is relatively higher than 160 points the previous year.
{{< /spoiler >}}

## Question 2
A study try to determine the relation between obesity and the response to pain. The obesity is measured as the percentage over the ideal weight ($X$), and the response to pain with a measure of the twinge sensation.
For a sample of 10 individuals we got the following sums:

$\sum x_i=737$, $\sum y_j=77$, $\sum x_i^2=55589$, $\sum y_j^2=799.5$, $\sum x_iy_j=6056.5$

1. Compute the linear regression model of the response to pain on the obesity.
2. What is the change in the response to pain for an increment of one point in the weight?
3. What percentage of the variability of the response to pain does not explain the linear regression model?
4. Taking into account the parameters of the exponential model given in the table below, give the equation of the exponential model.
Which transformation is required to convert this model into a linear one?

$$
\begin{array}{lr}
  \hline
  \mbox{Coefficient} & \mbox{Estimation}\newline
  \mbox{Intercept} & -1.772\newline
  x & 0.049\newline
  \hline
\end{array}
\qquad
\begin{array}{r}
  \hline
  R^2\newline
  0.72\newline
  \hline
\end{array}
$$

5. What is the expected response to pain for an obesity of 50\% according to the linear model?
And according to the exponential model?
Which prediction is more reliable?

{{< spoiler text="Solution" >}}
1. Linear model of response to pain on obesity: 
$\bar x=73.7$, $s_x^2=127.21$. 
$\bar y=7.7$, $s_y^2=20.66$. 
$s_{xy}=38.16$
Regression line of pain relief on obesity: $y=-14.41+0.3x$. 
2. For each increment of one unit in the obesity the response to pain will increase 0.3 units. 
3. Linear coefficient of determination: $r^2=0.554$. So, the linear model explains the 55.4% of the variability of the response to pain and it does not explain the remaining 44.6%.
4. Exponential regression model: $y=e^{-1.772+0.049x}$. To compute this model you have to apply the logarithm to the dependen variable, that is, the response to pain and then compute the regression line of the logarithm of the response to pain on obesity. 
5. Prediction with the linear model: $y(50)=0.59$ 
Prediction with the exponential model: $y(50)=1.9699$ 
The prediction with the exponential model is better as the exponential coefficient of determination is greater than the linear one. 
{{< /spoiler >}}

