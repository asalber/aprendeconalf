---
title: Physiotherapy exam 2022-05-06
date: 2022-05-06
tags: [Exam, Statistics, Biostatistics, Physiotherapy]
categories: [Statistics, Biostatistics]
type: book
---

Degrees: Physiotherapy  
Date: May 6, 2022

## Question 1

A basketball player scores 12 points per game on average. 

1. What is the probability that the player scores more than 4 points in a quarter? 

2. If the player plays 10 games in a league, what is the probability of scoring less than 6 points in some game? 

{{< spoiler text="Show solution" >}}
1. Let $X$ be the points scored in a quarter by the player. Then $X\sim P(3)$, and $P(X>4)=0.1847$. 

2. Let $Y$ be the number of points scored in a game by the player. Then $Y\sim P(12)$ and $P(Y<6)=0.0203$.  
Let $Z$ be the number of games with less than 6 points scored by the player. Then $Z\sim B(10, 0.0203)$, and $P(Z>0)=0.1858$. 
{{< /spoiler >}}

## Question 2

8% of people in a population consume cocaine. It is also known that 4% of people who consume cocaine have a heart attack and 10% of people who have a heart attack consume cocaine. 

1. Construct the probability tree for the random experiment of drawing a random person from the population and measuring if he or she consumes cocaine and if he or she has a heart attack. 

2. Compute the probability that a random person of the population does not consume cocaine and does not have a heart attack. 

3. Are the events of consuming cocaine and having a heart attack dependent? 

4. Compute the relative risk and the odds ratio of suffering a heart attack consuming cocaine. Which association measure is more suitable for this study? Interpret it. 


{{< spoiler text="Show solution" >}}
Let $C$ the event of consuming cocaine and $H$ the event of having a heart attack. 

1. <img src="../img/probability-tree-cocaine.svg" width="500px"/>

2. $P(\overline C\cap \overline H)=0.8912$. 

3. The events are dependent as $P(C)=0.08\neq P(C|H)=0.1$. 

4. $RR(H)=1.2778$ and $OR(H)=1.2894$. The odds ratio is more suitable as the study is retrospective. That means that the odds of having a heart attack is $1.2894$ times greater if a person consumes cocaine. 
{{< /spoiler >}}

## Question 3

The creatine phosphokinase (CPK3) is an enzyme in the body that causes the phosphorylation of creatine. This enzyme is found in the skeletal muscle and can be measured in a blood analysis. The concentration of CPK3 in blood is normally distributed, and the interval centred at the mean with the reference values, that accumulates 99% of the population, ranges from 40 to 308 IU/L in healthy adult males. 

1. Compute the mean and the standard deviation of the concentration of CPK3 in healthy males.

2. A diagnostic test to detect muscular dystrophy gives a negative outcome when the concentration of CPK3 is below 300 UI/L. Compute the specificity of the test. 

3. If the concentration of CPK3 in people with muscular dystrophy also follows a normal distribution with mean 350 IU/L and the same standard deviation, what is the sensitivity of the test? 

4. Compute the predictive values of the test and interpret them assuming that the muscular dystrophy prevalence is 8%.

{{< spoiler text="Show solution" >}}
1. $\mu = 174$ IU/L and $\sigma = 51.938$ IU/L. 

2. Specificity = $0.9924$. 

3. Sensitivity = $0.8321$.  
The test is better to confirm the disease as the specificity is greater than the sensitivity. 

4. PPV = $0.9046$. Thus, we can diagnose the disease with a positive outcome.  
NPV = $0.9855$. Thus, we can rule out the disease with a negative outcome.
{{< /spoiler >}}