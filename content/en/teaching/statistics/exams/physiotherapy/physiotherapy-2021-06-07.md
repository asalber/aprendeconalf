---
title: Physiotherapy exam 2021-06-07
date: 2021-06-07
tags: [Exam, Statistics, Biostatistics, Physiotherapy]
categories: [Statistics, Biostatistics]
type: book
---

Degrees: Physiotherapy  
Date: June 7, 2021

## Probability and random variables

### Question 1

The average number of injuries in an international tennis tournament is 2.

1. Compute the probability that in an international tennis tournament there are more than 2 injuries.

2. If a tennis circuit has 6 international tournaments, what is the probability that there are no injuries in some of them?

{{< spoiler text="Show solution" >}}
1. Let $X$ be the number of injuries in a tournament, then $X\sim P(2)$ and $P(X>2)=0.3233$.

2. Let $Y$ be the number of tournaments in the tennis circuit with no injuries, then $Y\sim B(6,0.1353)$ and $P(Y>0)=0.5821$.
{{< /spoiler >}}

### Question 2

The tables below corresponds to two tests $A$ and $B$ to detect an injury that have been applied to the same sample. 

$$
\begin{array}{lcc} 
\hline 
\mbox{Test A} & \mbox{Injury} & \mbox{No injury} \newline
\mbox{Outcome } + & 87 & 14 \newline
\mbox{Outcome }- & 33 & 866 \newline
\hline
\end{array} 
\qquad 
\begin{array}{lcc}
\hline
\mbox{Test B}& \mbox{Injury} & \mbox{No injury} \newline
\mbox{Outcome }+ & 104 & 115 \newline
\mbox{Outcome }- & 16 & 765 \newline
\hline
\end{array}
$$

1. Which test is more sensitive? Which one is more specific?

2. According to the predictive values, which test is better to diagnose the injury? Which one is better to rule out the injury?

3. Assuming that both tests are independent, what is the probability of getting a right diagnose with both tests if we apply both tests to a healthy person?

4. Assuming that both tests are independent, what is the probability of getting at least a positive outcome if we apply both tests to a random person?

{{< spoiler text="Show solution" >}}
Let $D$ the event of suffering the injury, and $+$ and $-$ the events of getting a positive and a negative outcome in the test, respectively.

1. Test $A$: sen = $0.725$ and spe = $0.9841$.  
Test $B$: sen = $0.8667$ and spe = $0.8693$.  
Thus, test $A$ is more specific and test $B$ is more sensitive.

2. Test $A$: PPV = $0.8614$ and NPV = $0.9633$.  
Test $B$: PPV = $0.4749$ and NPV = $0.9795$.  
Thus, test $A$ is better to diagnose the injury and test $B$ is better to rule out the injury.

3. $P(-_A\cap -_B | \overline{D}) = 0.8555$.

4. $P(+_A\cup +_B) = 0.2979$.
{{< /spoiler >}}

### Question 3

A study tries to determine the effect of a low fat diet in the lifetime of rats. The rats where divided into two groups, one with a normal diet and another with a low fat diet. It is assumed that the lifetimes of both groups are normally distributed with the same variance but different mean. If 20% of rats with normal diet lived more than 12 months, 5% less than 8 months, and 85% of rats with low fat diet lived more than 11 months,

1. Compute the means and the standard deviation of the lifetime of rats following a normal diet and a low fat diet?

2. If 40% of the rats were under a normal diet, and 60% of rats under a low fat diet, what is the probability that a random rat die before 9 months?

{{< spoiler text="Show solution" >}}
Let $X$ be the life time of a random rat, and let $X_1$ and $X_2$ be the lifetime of rats with a normal diet and a low fat diet respectively,

1. $\mu_1=10.6461$ months, $\mu_2=12.6673$ months and $s=1.6087$ months.

2. $P(X<9)=0.068$. 
{{< /spoiler >}}

