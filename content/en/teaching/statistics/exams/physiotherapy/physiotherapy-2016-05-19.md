---
title: Physiotherapy exam 2016-05-19
date: 2016-05-19
tags: [Exam, Statistics, Biostatistics]
categories: [Statistics, Biostatistics, Physiotherapy]
type: book
---

Grade: Physiotherapy  
Date: May 19, 2016

## Question 1

To check if the recovery time from a patellar tendonitis with a physioterapy treatment depends on gender, a sample of 390 patients (210 males and 180 females) was drawn and the recovery time was measured for every patient. The table below shows the frequencies of times. 

$$
\begin{array}{ccc}
\hline
\mbox{Time (days)} & \mbox{Males} & \mbox{Females}\newline
20-30 & 50 & 73\newline
30-40 & 61 & 42\newline
40-50 & 26 & 31\newline
50-60 & 32 & 20\newline
60-70 & 20 & 12\newline
70-80 & 11 & 2\newline
80-90 & 10 & 0\newline
\hline
\end{array}
$$
 
1. Calculate the mean of recovery time for males, females and for the whole sample. What mean is more representative the mean of the recovery time of males or the one of females? Justify the answer. 
2. What distribution is more symmetric, the distribution of recovery time of males or the one of females?
3. Compare the kurtosis of the recovery time of males and females. 
4. Calculate the 80th percentile of the recovery time of males. 
5. What percentage of females will have a recovery time greater than 63 days?

Use the following sums for the calculations,
Males: $\sum x_in_i = 9290$ days, $\sum x_i^2n_i=474050$ days$^2$, $\sum(x_i-\bar x)^3n_i = 812271.3832$ days$^3$ and $\sum(x_i-\bar x)^4n_i = 48895722.3971$ days$^4$.
Females: $\sum x_in_i = 6720$ days, $\sum x_i^2n_i=282300$ days$^2$, $\sum(x_i-\bar x)^3n_i = 347773.3333$ days$^3$ and $\sum(x_i-\bar x)^4n_i = 14802393.3333$ days$^4$.

{{< spoiler text="Solution" >}}
1. Males: $\bar x_m=44.2381$ days, $s^2_m=300.3719$ days$^2$, $s_m=17.3312$ days and $cv_m=0.3918$. 
Females: $\bar x_f=37.3333$ days, $s^2_f=174.5556$ days$^2$, $s_f=13.2119$ days and $cv_f=0.3539$. 
Thus, is more representative the mean of females. 
2. $g_{1m}=0.743$ and  $g_{1f}=0.8378$. Thus, both distributions are right-skewed but is more symmetric the distribution of males. 
3. $g_{2m}=-0.4193$ and  $g_{2f}=-0.3011$. Thus, both distributions are platykurtic, but the disribution of males is flatter. 
4. $P_{80}=59.7041$ days. 
5. $16.68\%$.
{{< /spoiler >}}


## Question 2
To check if the recovery time from a patellar tendonitis with a physioterapy treatment depends on age, a sample of 8 patients was drawn and the recovery time $Y$ (in days) and ages $X$ (in years) were measured for every patient. The table below shows the results.

| Age (years)| Recovery time (days)|
|-----------:|--------------------:|
|          32|                   20|
|          38|                   25|
|          48|                   32|
|          51|                   40|
|          57|                   55|
|          61|                   75|
|          68|                  102|
|          71|                  130|

1. Calculate the regresion line of the recovery time on the age. 
2. According to the linear regression model, what is expected age for a patient with a recovery time of 100 days? 
3. Calculate the exponential regression model of the recovery time on age. 
4. What regression model explains better the relation between the recovery time and the age, the exponential or the linear? Justify the answer. 
Use the following sums for the calculations:
$\sum x_i=426$, $\sum \log(x_i)=31.5425$, $\sum y_j=479$, $\sum \log(y_j)=31.1866$,
$\sum x_i^2=24008$, $\sum \log(x_i)^2=124.909$, $\sum y_j^2=39603$, $\sum \log(y_j)^2=124.7374$,
$\sum x_iy_j=29042$, $\sum x_i\log(y_j)=1724.5468$, $\sum \log(x_i)y_j=1956.6274$, $\sum \log(x_i)\log(y_j)=124.2263$.

{{< spoiler text="Solution" >}}

1. Linear model
$\bar x=53.25$ years, $s_x^2=165.4375$ years$^2$. 
$\bar y=59.875$ days, $s_y^2=1365.3594$ days$^2$. 
$s_{xy}=441.9062$ years$\cdot$days. 
Regression line of recovery time on age: $y=-82.3631 + 2.6711x$. 


2. $66.2367$ years. 

3. Exponential model
$\overline{\log(y)}=3.8983$ log(days), $s_{\log(y)}^2=0.3953$ log(days)$^2$. 
$s_{x\log(y)}=7.9829$ years$\cdot$log(days). 
Exponential model of recovery time on age: $y=e^{1.3288 + 0.0483x}$. 
4. Linear coefficient of determination $r^2=0.8645$. 
Exponential coefficient of determination $r^2=0.9745$. 
So the exponential model fits better.
{{< /spoiler >}}

## Question 3


In a random sample of 500 people drawn from a population there are 20 persons with an injury $A$, 40 persons with other injury $B$ and 450 persons with none of the injuries.
Use relative frequencies to estimate probabilities in following questions:

1. Calculate the probability that a person has both injuries
2. Calculate the probability that a person has some injury.
3. Calculate the probability that a person has injury $A$ but no $B$.
4. Calculate the probability that a person has injury $A$ if he or she has injury $B$.
5. Calculate the probability that a person has injury $B$ if he or she doesn't have injury $A$.
6. Are the injuries $A$ and $B$ dependent?

{{< spoiler text="Solution" >}}
1. $P(A\cap B) = 0.02$. 
2. $P(A\cup B) = 0.1$. 
3. $P(A-B) = 0.02$. 
4. $P(A|B) = 0.25$. 
5. $P(B|\bar A) = 0.0625$. 
6. The injuries are dependent. 
{{< /spoiler >}}

## Question 4
The level of severity $X$ of an injury is classified in a scale from 1 to 5, from low to high severity.
The probability distribution of $X$ in a population is plotted below. 

<img src="../img/severity_probability_function-1.svg" title="plot of chunk severity_probability_function" alt="plot of chunk severity_probability_function" style="display: block; margin: auto;" />


1. Calculate and plot the distribution function.
2. Calculate the following probabilities: $P(X\leq 2)$, $P(X>3)$, $P(X=4.2)$ and $P(1<X\leq 4.2)$.
3. Calculate the mean and the standard deviation of $X$. Is the mean representative?
4. If a level of severity of 0.05 is considered incurable, what is the probability of having some person with an incurable injury in a sample of 10 persons with the injury?
5. If there are 6 persons injuried per month in average, what is the probabilitiy of having more than 2 persons injuried? What is the probability of having more than 1 person injuried with an incurable injury?

{{< spoiler text="Solution" >}}
1. $$F(x) = 
\begin{cases}
0 & \mbox{if } x<1\newline
0.2 & \mbox{if } 1\leq x< 2\newline
0.6 & \mbox{if } 2\leq x< 3\newline
0.85 & \mbox{if } 3\leq x< 4\newline
0.95 & \mbox{if } 4\leq x< 5\newline
1 & \mbox{if } x\geq 5
\end{cases}
$$
<img src="../img/severity_distribution_function-1.svg" title="plot of chunk severity_distribution_function" alt="plot of chunk severity_distribution_function" style="display: block; margin: auto;" />
2. $P(X\leq 2)=0.6$, $P(X>3)=0.15$, $P(X=4.2)=0$, $P(1<X\leq 4.2)=0.75$ 

3. $\mu = 2.4$ and $s=1.0677$. The mean is moderately representative because $cv=0.4449$. 
4. Naming $X$ to the number of persons having an incurable injury in a sample of 10 persons with the injury, $P(X\geq 1)=0.4013$. 
5. Naming $Y$ to the number of persons injuried in a month, $P(T>2)=0.938$. 
Naming $Z$ to the number of persons injuried with an incurable injury in an month, $P(T>1)=0.0369$. {{< /spoiler >}}

## Question 5


A diagnostic test to determine doping of athletes returns a positive outcome when the concentration of a substance in blood is greater than 4 $\mu$g/ml. If the distribution of the substance concentration in doped athletes follows a normal distribution model with mean 4.5 $\mu$g/ml and standard deviation 0.2 $\mu$g/ml, and in non-doped athletes follow a normal distribution model with mean 3 $\mu$g/ml and standard deviation 0.3 $\mu$g/ml,

1.  what is the sensitivity and specificity of the test?
2.  If there are a 10% of doped athletes in a competition, what are the predicted values?

{{< spoiler text="Solution" >}}
Naming $D$ to the event of being doped, $X$ to the concentration in doped athletes and $Y$ to the concentration in non-doped athletes, 
1. Sensitivity $P(+\vert D) = P(X>4)=0.9938$ and specificity $P(-\vert \bar D)=P(Y<4)=0.9996$ 
2. PPV $P(D\vert +) = 0.9961$ and NPV $P(\bar D\vert -) = 0.9993$
{{< /spoiler >}}

