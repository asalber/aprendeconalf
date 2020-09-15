---
title: Physiotherapy exam 2017-05-19
date: 2017-05-19
tags: [Exam, Statistics, Biostatistics, Physiotherapy]
categories: [Statistics, Biostatistics]
type: book
---

Degrees: Physiotheraphy  
Date: May 19, 2017

# Probability and random variables

## Question 1

The prevalence of sciatica in a population is 3%.
The Lasegue's test is a neurotension test that is used to diagnose the sciatica with a sensitivity of 91% and a specificity of 26%.
On the other hand, there is an alternative test with a sensitivity of 80% and a specificity of 90%.

1. Compute the positive predictive value for the Lasegue's test.
2. Assuming that the tests are independent, compute the probability of having a positive outcome in both tests.
3. Compute the probability of getting a wrong diagnose in the Lesegue's test or in the alternative test.
4. Which test is better as a screening test (to rule out the sciatica)?



{{< spoiler text="Solution" >}}
1. $PPV=P(D|+)=0.0366$. It is not a goot test to confirm the sciatica as the post test probability of having the sciatica for a positive outcome is very low. 
2. Naming $L⁺$ to the event of having a positive outcome in Lasegue's test and $A⁺$ to the event of having a positive outcome in the alternative test: $P(L^+\cap A^+)=P(L^+)P(A^+)=0.7451\cdot 0.121 = 0.0902$. 
3. Naming $WL$ to the event of having a wrong diagnose with Lasegue's test and $WA$ to the event of having a wrong diagnose with the alternative test: $P(WL\cup WA)=P(WL)+P(WA)-P(WL\cap WA)=0.7205+ 0.103-0.7205\cdot0.103=0.7493$. 
4. Lesegue test: $NPV=P(\overline D|-)=0.9894$.
Alternative test: $NPV=P(\overline D|-)=0.9932$.
Thus, the alternative test is better to rule out the sciatica. 
{{< /spoiler >}}

## Question 2
A physiotherapist opens a clinic and use the social networks to advertise it.
In particular he send a friend request to 20 contacts on Facebook.
If the probability that a Facebook user accept the friend request is 80%, what is the probability that more than 18 accept the friend request?
What is the expected number of friend requests accepted?



{{< spoiler text="Solution" >}}
Naming $X$ to the number of accepted friend request, $X\sim B(20,0.8)$ and $P(X>18)=0.0692$.
The expected number of accepted friend request is $16$. 
{{< /spoiler >}}

## Question 3
According to a study of the Information Society of Spain in 2013, the spanish checks the mobile phone 150 times a day in average.
What is the probability that a spanish person checks the mobile phone more than 2 times an hour?



{{< spoiler text="Solution" >}}
1. Naming $X$ to the number of times that a spanish person checks the phone in an hour, $X\sim P(6.25)$ and $P(X>2)=0.9483$.
{{< /spoiler >}}

## Question 4
The the cervical rotation in a population follows a normal probability distribution model with mean 58º and standard deviation 6º.

1. Between what values are the cervical rotation of the central 50\% of the population?
2. Taking into account the precision of the measurement instrument, a goniometer, a rotation less than 53º is considered a mobility limitation.
If we take a random sample of 100 persons from this population, what is the expected number of persons with mobility limitation in the sample?



{{< spoiler text="Solution" >}}
Naming $X$ to the cervical rotation, $X\sim N(58, 6)$. 
1. $(Q1,Q3)=(53.9531, 62.0469)$. 
3. $P(X<53)=0.2023$ and the expected number of persons with mobility limitation in a sample of 100 persons is $20.2328$. 
{{< /spoiler >}}


