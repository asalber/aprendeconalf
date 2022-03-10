---
title: Physiotherapy exam 2019-05-27
date: 2019-05-27
tags: [Exam, Statistics, Biostatistics]
categories: [Statistics, Biostatistics, Physiotherapy]
type: book
---

Degrees: Physiotherapy  
Date: May 27, 2019

# Descriptive Statistics and Regression

## Question 1

A study tries to determine the effect of smoking during the pregnancy in the weight of newborns.
The table below shows the daily number of cigarretes smoked by mothers ($X$) and the weight of the newborn (all of them are males) ($Y$).

$$
\begin{array}{lrrrrrrrrrrrr}
\hline
\mbox{Daily num cigarettes} & 10.00 & 14.00 & 8.00 & 11.00 & 7.00 & 6.00 \newline
\mbox{Weight (kg)} & 2.55 & 2.44 & 2.68 & 2.65 & 2.71 & 2.85 \newline
\hline
\end{array}
$$

$$
\begin{array}{lrrrrrrrrrrrr}
\hline
\mbox{Daily num cigarettes} & 2.00 & 5.00 & 9.00 & 9.00 & 4.00 & 6.00 \newline
\mbox{Weight (kg)} & 3.45 & 2.93 & 2.67 & 2.59 & 3.02 & 2.72 \newline
\hline
\end{array}
$$

1. Give the equation of the regression line of the weight of newborns on the daily number of cigarettes and interpret the slope.

2. Which regression model is better to predict the weight of newborns, the logarithmic or the exponential?

3. Use the best of the two previous regression models to predict the weight of a newborn whose mother smokes 12 cigarettes a day. Is this prediction reliable?

Use the following sums for the computations:  
$\sum x_i=91$ cigarettes, $\sum \log(x_i)=23.0317$ $\log(\mbox{cigarettes})$, $\sum y_j=33.26$ kg, $\sum \log(y_j)=12.1857$ $\log(\mbox{kg})$,  
$\sum x_i^2=809$ cigarettes$^2$, $\sum \log(x_i)^2=47.196$ $\log(\mbox{cigarettes})^2$, $\sum y_j^2=92.9708$ kg$^2$, $\sum \log(y_j)^2=12.4665$ $\log(\mbox{kg})^2$,  
$\sum x_iy_j=243.61$ cigarettes$\cdot$kg, $\sum x_i\log(y_j)=89.3984$ cigarettes$\cdot\log(\mbox{kg})$, $\sum \log(x_i)y_j=62.3428$ $\log(\mbox{cigarettes})$kg,
$\sum \log(x_i)\log(y_j)=22.8753$ $\log(\mbox{cigarettes})\log(\mbox{kg})$.

{{< spoiler text="Solution" >}}
1. $\bar x=7.5833$ cigarettes, $s_x^2=9.9097$ cigarettes$^2$.
$\bar y=2.7717$ kg, $s_y^2=0.0654$ kg$^2$.
$s_{xy}=-0.7176.$ cigarettes$\cdot$kg
Regression line: $y=-0.0724x + 3.3208$.
The slope of the regression line is $b_{yx}=-0.0724$. That means that the weight of the newborn will decrease 0.0724 kg per daily cigarette smoked by the mother.

2. $\overline{\log(x)}=1.9193$ log(cigarettes), $s_{\log(x)}^2=0.2492$ log(cigarettes)$^2$.
$\overline{\log(y)}=1.0155$ log(kg), $s_{\log(y)}^2=0.0077$ log(kg)$^2$.
$s_{x\log(y)}=-0.2508$ cigarettes$\cdot$log(kg), $s_{\log(x)y}=-0.1245$ log(cigarettes)$\cdot$kg
Logarithmic coef. determination: $r^2=0.9499$
Exponential coef. determination: $r^2=0.8268$
Therefore, the logarithmic models fits better the data and is better to predict the weight.

3. Logarithmic regression model: $y=3.7301+-0.4994\log(x)$.
Prediction: $y(12)=2.4892$ kg. The coefficient of determination is high but the sample size small, so the prediction is not enterely reliable.
{{< /spoiler >}}

## Question 2
The table below summarize the time that took to the runners to reach the finish in a long-distance race in Madrid:

$$
\begin{array}{lr}
\mbox{Time (min)} & \mbox{Num runners}\newline
\hline
(30,35] & 15\newline
(35,40] & 35\newline
(40,45] & 40\newline
(45,50] & 10\newline
\hline
\end{array}$$

In a another race in Paris, the mean of time was 40 minutes, the standard deviation 5 minutes and the coefficient of skewness $0.75$.

1. What percentage of runners took less than 42 minutes to reach the finish in Madrid?

2. Compute and interpret the interquartile range of the time for Madrid race.

3. In which race the mean of the time is more representative?

4. In which race the time have a more symmetric distribution?

5. In which race a time of 39 minutes to reach the finish is relatively smaller?

Use the following sums for the computations: $\sum x_i=3975$ min, $\sum x_i^2=159875$ min$^2$, $\sum (x_i-\bar x)^3=-628.12$ min$^3$ y
$\sum (x_i-\bar x)^4=80701.95$ min$^4$.

{{< spoiler text="Solution" >}}

1. $F(42)=0.66$, thus approximately $66\%$ of runners finished before 42 minutes.

2. $Q_1=36.4286$ min, $Q_3=43.125$ min and $IQR=6.6964$ min. The central 50% of times fall in a range of $6.6964$ minutes.

3. Madrid statistics: $\bar x=39.75$ min, $s^2=18.6875$ min$^2$, $s=4.3229$ min and $cv=0.1088$.
Paris statistics: $cv=0.125$. Thus, the mean of time in Madrid is a little bit more representative since the coef. of variation is smaller.

4. $g_1=-0.0778$, that is closer to 0 than the distribution of times in Paris, thus the distribution of times in Madrid is more symmetric.

5. The standard score of the Madrid sample is $z(39)=-0.1735$ and the standard score of the Paris one $z(39)=-0.2$, thus a time of 39 min is relatively smaller in the sample of Paris.
  
{{< /spoiler >}}

# Probability and Random Variables

## Question 1
It has been observed that the concentration of a metabolite in urine can be used as a diagnostic test for a disease.
The concentration (in mg/dl) in healthy individuals follows a normal distribution with mean 90 and standard deviation 8, while in sick individuals follows a normal distribution with mean 120 and standard deviation 10.

1. If the cut-off point is set at 105 mg/dl (positive above and negative below), what is the sensitivity and the specificity of the test?

2. If the cut-off point is set at 105 mg/dl and we assume a prevalence of 10%, what is the probability of a correct diagnostic?

3. If we want a sensitivity of 95%, where must we set the cut-off point? What would the specificity of the test be?

{{< spoiler text="Solution" >}}
Let $X$ and $Y$ be the distributions of the concentration of metabolite in healthy and sick individuals respectively.

1. Sensitivity: $P(+|D) = P(Y>105) = 0.9332$.
Specificity: $P(-|\overline D) = P(X<105) = 0.9696$.

2. $P(\mbox{correct diagnostic}) = P(D\cap +) + P(\overline D \cap -) = 0.966$.

3. Cut-off point $103.5515$ mg/dl.
Specificity: $P(-|\overline D) = P(X<103.5515) = 0.9549$.

{{< /spoiler >}}

## Question 2
Let $A$ and $B$ be two events of a random experiment, such that $A$ is three times as likely as $B$, $P(A\cup B)=0.8$ and $P(A\cap B)=0.2$.

1. Compute $P(A)$ and $P(B)$.

2. Compute $P(A-B)$ and $P(B-A)$.

3. Compute $P(\bar A \cup \bar B)$ and $P(\bar A \cap \bar B)$.

4. Compute $P(A|B)$ and $P(B|A)$.

5. Are $A$ and $B$ independent?

{{< spoiler text="Solution" >}}

1. $P(A) = 0.75$ and $P(B) = 0.25$.

2. $P(A-B) = 0.55$ and $P(B-A) = 0.05$.

3. $P(\bar A \cup \bar B) = 0.8$ and $P(\bar A \cap \bar B) = 0.2$.

4. $P(A|B) = 0.8$ and $P(B|A) = 0.2667$.

5. No, they are dependent since $P(A|B)\neq P(A)$.

{{< /spoiler >}}

## Question 3
The employees of a courier company send an average of $246.2$ messages in a period of 12 hours. It is also known that the mean of messages sent by males is $256.2$ and by females is $237.4$ in the same period.

1. Compute the probability that a random person of the company sends 5 messages in a period of half an hour.

2. If we draw randomly 10 women of this company, what is the probability that at least 3 of them sends more than one message in a period of one hour?

3. If we draw randomly 100 men of this company, what is the probability that none of them sends less than 2 messages in a period of a quarter of an hour?

{{< spoiler text="Solution" >}}

1. Let $X$ be the number of messages sent in 1 hour. Then $X\sim P(10.2583)$ and $P(X=5)=0.0332$.

2. Let $Y$ be the number of women in a sample of 10 that sent more than 1 message in 1 hour. Then $Y\sim B(10, 1)$ and $P(Y\geq 3)=1$.

3. Let $Z$ be the number of men in a sample of 100 that sent less than 2 messages in a quarter of hour. Then $Z\sim B(100, 0.0305)$ and $P(Z=0)=0.0166$.

{{< /spoiler >}}