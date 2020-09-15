---
title: Problems Diagnostic Tests
linkTitle: Diagnostic Tests
date: 
lastmod:
tags: [Probability, Diagnostic Tests]
categories: [Statistics, Biostatistics, Epidemiology]
type: book
weight: 60
---

## Exercise 1

A test was applied to a sample of people in order to evaluate its effectiveness; the results are as follows:

$$
\begin{array}{l|cc}
& \mbox{Test }+ & \mbox{Test }- \newline
\hline
\mbox{Sick} & 2020 & 140 \newline

\mbox{Healthy} & 80 & 7760 \newline
\end{array}
$$

Calculate for this test:

1.  The sensitivity and the specificity.
2.  The positive and negative predictive value.
3.  The probability of a correct diagnosis.

{{< spoiler text="Solution" >}}
Naming $S$ and $H$ to the events of being sick and healthy respectively,  
1. Sensitivity $P(+\vert S)=0.9352$ and specificity $P(-\vert H)=0.9898$.  
2. PPV $P(S\vert +)=0.9619$ and NPV $P(H\vert -)=0.9823$.  
3. $P((S\cap +)\cup (H\cap -)) = P(S\cap +) + P(H\cap -) = 0.978$. 
{{< /spoiler >}}


## Exercise 2


We know, from a research study, that 10% of people over 50 suffer a particular type or arthritis. We have developed a new method to detect the disease and after clinical trials we observe that if we apply the method to people with arthritis we get a positive result in 85% of cases, while if we apply the method to people without arthritis, we get a positive result in 4% of cases. Answer the following questions:

1.  What is the probability of getting a positive result after applying the method to a random person?
2.  If the result of applying the method to one person has been positive, what is the probability of having arthritis?

{{< spoiler text="Solution" >}}
Naming $A$ to the event of having arthritis,  
1. $P(+)=0.121$.  
2. $P(A\vert +) = 0.7025$.
{{< /spoiler >}}

## Exercise 3


We have two different test $A$ and $B$ to diagnose a disease. Test $A$ have a sensitivity of 98% and a specificity of 80%, while test $B$ have a sensitivity of 75% and a specificity of 99%.

1.  Which test is better to confirm the disease?
2.  Which test is better to rule out the disease?
3.  Often a test is used to discard the presence of the disease in a large amount of people apparently healthy. This type of test is known as *screening test*. Which test will work better as a screening test? What are the predictive values of this test if the prevalence of the disease is 0.01? And if the prevalence of de disease is 0.2?
4.  The positive predictive value of a screening test used to be not too high. How can we combine the tests $A$ and $B$ to have a higher confidence in the diagnosis of the disease? Calculate the post-test probability of having the disease with the combination of both thest, if the outcome of both test is positive for a prevalence of 0.01.

{{< spoiler text="Solution" >}}
1. Test $B$ cause it has a greater specificity.  
2. Test $A$ cause it has a greater sensitivity.  
3. Test $A$ will perform better as a screening test.  
For a prevalence of $0.01$ the PPV is $P(D\vert +)=0.0472$ and the NPV is $P(\bar D\vert -)=0.9997$.  
For a prevalence of $0.2$ the PPV is $P(D\vert +)=0.5506$ and the NPV is $P(\bar D\vert -)=0.9938$.  
4. First applying test $A$ to everybody and then applying test $B$ to positive cases of test $A$.  
$P(D\vert +_A\cap +_B)=0.7878$.
{{< /spoiler >}}
