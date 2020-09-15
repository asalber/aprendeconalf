---
title: Physiotherapy exam 2019-06-18
date: 2019-06-18
tags: [Exam, Statistics, Biostatistics]
categories: [Statistics, Biostatistics, Physiotherapy]
type: book
---

Degrees: Physiotherapy  
Date: June 18, 2019

# Descriptive Statistics and Regression

## Question 1

A study tries to determine the effectiveness of an occupational risk prevention program in jobs that require to be sit a lot of hours.
A sample of individuals between 40 and 50 years that spent more than 5 hours sitting were drawn.
It was observed if they followed or not the occupational risk prevention program and the number of spinal injuries after 10 years.
The results are shown in the table below.

$$
\begin{array}{lrrrrrrrrrrrrrrr}
\hline
\mbox{With prevention program} & 1 & 3 & 2 & 4 & 4 & 0 & 2 & 4 & 2 & 2 & 5 & 2 & 3 & 2 & 0 \newline
\mbox{Wihtout prevention program} & 6 & 3 & 1 & 3 & 7 & 6 & 5 & 5 & 9 & 5 & 5 & 4 & 4 & 3 &  \newline
\hline
\end{array}$$

1. Plot the polygon of cumulative relative frequencies of the total sample.

2. According to the interquartile range, which sample has more central spread of the spinal injuries, the sample of people following the prevention program or the sample of people not following the prevention program?

3. Which sample has a greater relative spread with respect to the mean of the spinal injuries, the sample of people following the prevention program or the sample of people not following the prevention program?

4. Which sample has a more normal kurtosis of the number of spinal injuries, the sample of people following the prevention program or the sample of people not following the prevention program?

5. Which number of spinal injuries is relatively greater, 2 injuries of a person following the prevention program or 4 injuries of a person not following the prevention program?

Use the following sums for the computations:  
With prevention program: $\sum x_i=36$ injuries, $\sum x_i^2=116$ injuries$^2$, $\sum (x_i-\bar x)^3=-0.48$ injuries$^3$ and $\sum (x_i-\bar x)^4=135.97$ injuries$^4$.  
Without prevention program: $\sum y_i=66$ injuries, $\sum y_i^2=362$ injuries$^2$, $\sum (y_i-\bar y)^3=27.92$ injuries$^3$ and $\sum (y_i-\bar y)^4=586.9$ injuries$^4$.

{{< spoiler text="Solution" >}}
1. <img src="../img/des-fis-5-cumulative-frequencies-polygon.svg" title="Cumulative relative frequency polygon of spinal injuries" alt="Cumulative relative frequency polygon of spinal injuries" style="display: block; margin: auto;" width="600" />
2. With prevention program: $Q_1=2$ injuries, $Q_3=4$ injuries, $IQR=2$ injuries.
Without prevention program: $Q_1=3$ injuries, $Q_3=6$ injuries, $IQR=3$ injuries.
The sample not following the prevention program has more central spread since the interquartile range is greater.
3. With prevention program: $\bar x=2.4$ injuries, $s^2=1.9733$ injuries$^2$, $s=1.4048$ injuries and $cv=0.5853$.
Without prevention program: $\bar y=4.7143$ injuries, $s^2=3.6327$ injuries$^2$, $s=1.906$ injuries and $cv=0.4043$. 
The sample following the prevention program has a greater relative spread with respect to the mean since the coef. of variation is greater.
4. With prevention program: $g_2=-0.6722$.
Without prevention program: $g_2=0.1768$.
Thus the sample not following the prevention program has a more normal kurtosis, since the coeff. of kurtosis is closer to 0.
1. With prevention program: $z(2)=-0.2847$.
Without prevention program: $z(4)=-0.3748$.
Thus 4 injuries in the sample not following the prevention program is relatively smaller, since its standard score is smaller.
{{< /spoiler >}}

## Question 2
The evolution of the price of a muscle relaxant between 2015 and 2019 is shown in the table below.

$$
\begin{array}{lrrrrr}
\hline
\mbox{Year} & 2015 & 2016 & 2017 & 2018 & 2019 \newline
\mbox{Price (€)} & 1.40 & 1.60 & 1.92 & 2.30 & 2.91 \newline
\hline
\end{array}$$

1. Which regression model is better to predict the price, the linear or the exponential?

2. Use the best of the two previous models to predict the price in 2020.

{{< spoiler text="Solution" >}}
1. $\bar x=2017$ years, $s_x^2=2$ years$^2$.
$\bar y=2.026$ €, $s_y^2=0.2882$ €$^2$.
$\overline{\log(y)}=0.672$ log(€), $s_{\log(y)}^2=0.0673$ log(€)$^2$.
$s_{xy}=0.744$ years$\cdot$€, $s_{x\log(y)}=0.3653$ years$\cdot\log(€)$
Linear coef. determination: $r^2=0.9603$
Exponential coef. determination: $r^2=0.9909$
Thus the exponential regression model is better to predict the price since the coef. of determination is greater.
2. Exponential regression model: $y=e^{-367.6861+0.1826x}$.
Prediction: $y(2020)=3.3867$ €.
{{< /spoiler >}}

## Question 3

In a linear regression study between two variables $X$ and $Y$ we know $\bar x = 3$, $s_x^2=2$, $s_y^2=10.8$ and the regression line of $Y$ on $X$ is $y=90.9-2.3x$.

1. Compute the mean of $Y$.

2. Compute and interpret the linear correlation coefficient.

{{< spoiler text="Solution" >}}
1. $\bar y = 84$.
2. $r=-0.9898$.
{{< /spoiler >}}

# Probability and Random Variables

## Question 4
A study tries to determine the effectiveness of an occupational risk prevention program in jobs that require to be sit a lot of hours.
A sample of 500 individuals between 40 and 50 years that spent more than 5 hours sitting was drawn.
Half of the individuals followed the prevention program (treatment group) and the other half not (control group).
After 5 years it was observed that 12 individuals suffered spinal injuries in the group following the prevention program while 32 individuals suffered spinal injuries in the other group.
In the following 5 years it was observed that 21 individuals suffered spinal injuries in the group following the prevention program while 48 individuals suffered spinal injuries in the other group.

1. Compute the cumulative incidence of spinal injuries in the total sample after 5 years and after 10 years.

2. Compute the absolute risk of suffering spinal injuries in 10 years in the treatment and control groups.

3. Compute the relative risk of suffering spinal injuries in 10 years in the treatment group compared to the control group. Interpret it.
   
4. Compute the odds ratio of suffering spinal injuries in 10 years in the treatment group compared to the control group. Interpret it.

5. Which statistics, the relative risk or the odds ratio, is more suitable in this study? Justify the answer.

{{< spoiler text="Solution" >}}
Let $D$ be the event of suffering spinal injuries.

1. Cumulative incidence after 5 years: $R(D)=0.088$.
Cumulative incidence after 10 years: $R(D)=0.226$.

2. Risk in the treatment group: $R_T(D)=0.132$.
Risk in the control group: $R_C(D)=0.32$.

3. $RR(D)=0.4125$. Thus, the risk of suffering spinal injuries is less than half following the prevention program.

4. $OR(D)=0.3232$. Thus, the odd of suffering spinal injuries is less than one third following the prevention program.

5. Since the study is prospective and we can estimate the prevalence of $D$, both statistics are suitable, but relative risk is easier to interpret.
{{< /spoiler >}}

## Question 5
The table below shows the results of a study to evaluate the usefulness of a reactive strip to diagnose an urinary infection.

$$
\begin{array}{ccc}
\hline
\mbox{Outcome} & \mbox{Infection} & \mbox{No infection}\newline
\mbox{Positive} & 60 & 80\newline
\mbox{Negative} & 10 & 200\newline
\hline
\end{array}
$$

1. Compute the sensitivity and the specificity of the test.

2. Compute the positive and the negative predictive values.  
   Is this test better to confirm or to rule out the infection?

3. If another study has determined that the true prevalence of the infection is 2%, how does this affect to the predictive values?

{{< spoiler text="Solution" >}}
Let $D$ be the event corresponding to suffering the urinary infection and $+$ and $-$ the events corresponding to get a positive and negative outcome in the test respectively.

1. Sensitivity = $0.8571$ and Specificity = $0.7143$.

2. $PPV=0.4286$ and $NPV=0.9524$. Since the $PPV<NPV$ the test is better to rule out the infection.

3. $PPV=0.0577$ and $NPV=0.9959$. The positive predictive value descreases a lot while the negative predictive value increases al little bit.
{{< /spoiler >}}

## Question 6
The time required to recover from an injury follows a normal distribution with variance 64 days.  
It is also known that 10% of people with this injury require more than 80 days to recover.

1. What is the expected time required to recover from the injury?  

2. What percentage of individuals will require between 60 and 75 days to recover?

3. If we draw a random sample of 12 individuals with this injury, what is the probability of having between 9 and 11 individuals, both included, requiring less than 80 days to recover?

4. If we draw a random sample of 500 individuals with this injury, what is the probability of having less than 4 requiring a time above the 99th percentile to recover?

{{< spoiler text="Solution" >}}
Let $X$ be the time required to recover from the injury. Then $X\sim N(\mu, 8)$.

1. $\mu=69.7476$ days.

2. $P(60<X<75) = 0.6327$.

3. Let $Y$ be the number of individuals with the injury requiring less than 80 days to recover in a sample of 12. Then $Y\sim B(12, 0.9)$ and $P(9\leq Y\leq 11)=0.6919$.

4. Let $Z$ be the number of individuals with the injury requiring a time above the 99th percentile to recover in a sample of 500. Then $Z\sim B(500, 0.01)\approx P(5)$ and $P(Z\leq 4)=0.265$.
{{< /spoiler >}}