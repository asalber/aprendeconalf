---
title: Problems of Discrete Random Variables
linkTitle: Discrete Random Variables
date: 
lastmod: 
tags: [Random Variables, Discrete Random Variables]
categories: [Statistics, Biostatistics]
type: book
weight: 70
---

## Exercise 1
Let $X$ be a discrete random variable with the following probability distribution

$$
\begin{array}{|c|c|c|c|c|c|}
\hline
X & 4 & 5 & 6 & 7 & 8 \newline 
\hline
f(x) & 0.15 & 0.35 & 0.10 & 0.25 & 0.15 \newline 
\hline
\end{array}
$$

1.  Calculate and represent graphically the distribution function.
2.  Calculate the following probabilities
    a.  $P(X<7.5)$.
    b.  $P(X>8)$.
    c.  $P(4\leq X\leq 6.5)$.
    d.  $P(5<X<6)$.

{{< spoiler text="Solution" >}}
1. $$
F(x)=
\begin{cases}
0 & \text{if $x<4$,}\newline
0.15 & \text{if $4\leq x<5$,}\newline
0.5 & \text{if $5\leq x<6$,}\newline
0.6 & \text{if $6\leq x<7$,}\newline
0.85 & \text{if $7\leq x<8$,}\newline
1 & \text{if $8\leq x$.}
\end{cases}
$$  
2. $P(X<7.5)=0.85$, $P(X>8)=0$, $P(4\leq x\leq 6.5)=0.6$ and $P(5<X<6)=0$.
{{< /spoiler >}}


## Exercise 2
Let $X$ be a discrete random variable with the following probability distribution 

$$
F(x)=
\begin{cases}
0 & \text{if $x<1$,} \newline
1/5 & \text{if $1\leq x< 4$,} \newline
3/4 & \text{if $4\leq x<6$,} \newline
1 & \text{if $6\leq x$.}
\end{cases}
$$

1.  Calculate the probability function.
2.  Calculate the following probabilities
    a.  $P(X=6)$.
    b.  $P(X=5)$.
    c.  $P(2<X<5.5)$.
    d.  $P(0\leq X<4)$.
3.  Calculate the mean.
4.  Calculate the standard deviation.

{{< spoiler text="Solution" >}}


1. $$
\begin{array}{|c|c|c|c|c|c|}
\hline
X & 1 & 4 & 6 \newline 
\hline
f(x) & 0.2 & 0.55 & 0.25 \newline 
\hline
\end{array}
$$

2. $P(X=6)= 0.25$, $P(X=5)=0$, $P(2<X<5.5)=0.55$ and $P(0\leq X<4)=0.2$.  
3. $\mu=3.9$.  
4. $\sigma=1.6703$.
{{< /spoiler >}}


## Exercise 3
An experiment consist in injecting a virus to three rats and checking if they survive or not. It is known that the probability of surviving is $0.5$ for the first rat, $0.4$ for the second and $0.3$ for the third.

1.  Calculate the probability function of the variable $X$ that measures the number of surviving rats.
2.  Calculate the distribution function.
3.  Calculate $P(X\leq 1)$, $P(X\geq 2)$ and $P(X=1.5)$.
4.  Calculate the mean and the standard deviation. Is representative the mean?

{{< spoiler text="Solution" >}}
1. $$
\begin{array}{|c|c|c|c|c|}
\hline
X & 0 & 1 & 2 & 3 \newline
\hline
f(x) & 0.21 & 0.44 & 0.29 & 0.06\newline
\hline
\end{array}
$$

2.$$
F(x)=
\begin{cases}
0 & \text{si $x<0$,}\newline
0.21 & \text{si $0\leq x<1$,}\newline
0.65 & \text{si $1\leq x<2$,}\newline
0.94 & \text{si $2\leq x<3$,}\newline
1 & \text{si $3\leq x$.}
\end{cases}
$$

3. $P(X\leq 1)=0.65$, $P(X\geq 2)=0.35$ and $P(X=1.5)=0$.  
4. $\mu=1.2$ rats, $\sigma^2=0.7$ rats$^2$ y $\sigma=0.84$ rats.
{{< /spoiler >}}


## Exercise 4


The chance of being cured with certain treatment is 0.85. If we apply the treatment to 6 patients,

1.  What is the probability that half of them get cured?
2.  What is the probability that a least 4 of them get cured?

{{< spoiler text="Solution" >}}
Let $X$ be the number of cured patients,  
1. $P(X=3) = 0.0415$.  
2. $P(X\geq 4)= 0.9527$.
{{< /spoiler >}}


## Exercise 5


Ten persons came into contact with a person infected with tuberculosis. The probability of being infected after contacting a person with tuberculosis is 0.1.

1.  What is the probability that nobody is infected?
2.  What is the probability that at least 2 persons are infected?
3.  What is the expected number of infected persons?

{{< spoiler text="Solution" >}}
Let $X$ be the number of persons infected,  
1. $P(X=0) = 0.3487$.  
2. $P(X\geq 2)= 0.2639$.  
3. $\mu=1$.
{{< /spoiler >}}


## Exercise 6


The probability of suffering an adverse reaction to a vaccine is 0.001. If 2000 persons are vaccinated, what is the probability of suffering some adverse reaction?

{{< spoiler text="Solution" >}}
Let $X$ be the number of adverse reactions, $P(X\geq 1)=0.8648$.
{{< /spoiler >}}


## Exercise 7


The average number of calls per minute received by a telephone switchboard is 120.

1.  What is the probability of receiving less than 4 calls in 2 seconds?
2.  What is the probability of receiving at least 3 calls in 3 seconds?

{{< spoiler text="Solution" >}}
1. Let $X$ be the number of calls in 2 seconds, $P(X<4)=0.4335$.  
2. Let $Y$ be the number of calls in 3 seconds, $P(X\geq 3)= 0.938$.
{{< /spoiler >}}


## Exercise 8


A test contains 10 questions with 3 possible options each. For every question you get a point if you give the right answer and lose half a point if the answer is wrong. A student knows the right answer for 3 of the 10 questions and answers the rest randomly. What is the probability of passing the exam?

{{< spoiler text="Solution" >}}
Let $X$ be the number of correct answers in questions randomly answered, $P(X\geq 4)=0.1733$.
{{< /spoiler >}}


## Exercise 9


It has been observed experimentally that 1 of every 20 trillions of cells exposed to radiation mutates becoming carcinogenic. We know that the human body has approximately 1 trillion of cells by kilogram ot tissue. Calculate the probability that a 60 kg person exposed to radiation develops cancer. If the radiation affects 3 persons weighing 60 kg, what is the probability that a least one of them develops cancer?

{{< spoiler text="Solution" >}}
Let $X$ be the number of cells mutated, $P(X>0)=0.9502$.  
Let $Y$ be the of persons developing cancer, $P(Y\geq 1) = 0.9999$.
{{< /spoiler >}}


## Exercise 10


A diagnostic test for a disease returns 1% of positive outcomes, and the positivie and negative predictive values are 0.95 and 0.98 respectively.

1.  Calculate the prevalence of the disease.
2.  Calculate the sensitivity and the specificity of the test.
3.  If the test is applied to 12 sick persons, what is the probability of getting at least a wrong diagnosis?
4.  If the test is applied to 12 persons, what is the probability of getting a right diagnosis for all of them?

{{< spoiler text="Solution" >}}
1. $P(D)=0.0293$.  
2. Sensitivity $P(+\vert D)=0.3242$ and specificity $P(-\vert \bar D)=0.9995$.  
3. Let $X$ be the number of wrong diagnosis in 12 sick persons, $P(X\geq 1)=1$.  
4. Let $Y$ be the number of right diagnosis in 12 persons, $P(X=12)=0.7818$.
{{< /spoiler >}}


## Exercise 11


In a study about a parasite that attacks the kidney of rats it is known that the average number of parasites per kidney is 3.

1.  Calculate the probability that a rat has more than 3 parasites.
2.  Calculate the probability of having at least 9 rats infected in a sample of 10 rats.

{{< spoiler text="Solution" >}}
1. Let $X$ be the number of parasites in a rat, $P(X>3)=0.8488$.  
2. Let $Y$ be the number of rats with parasites in a sample of 10 rats, $P(Y\geq 9)=0.9997$.
{{< /spoiler >}}


## Exercise 12


In a physiotherapy course there are 60% of females and 40% of males.

1.  If 6 random students have to go to a hospital for making practices, what is the probability of going more males than females?
2.  In 5 samples of 6 students, what is the probability of having some sample without males?

{{< spoiler text="Solution" >}}
1. Let $X$ be the number of females in a group of 6 students, $P(X<2)=0.1792$.  
2. Let $Y$ be the number of groups of 6 students without males in a sample of 5 groups, $P(Y>0) =0.2125$.
{{< /spoiler >}}



