---
title: Physiotherapy exam 2016-05-13
date: 2016-05-13
tags: [Exam, Statistics, Biostatistics]
categories: [Statistics, Biostatistics, Physiotherapy]
type: book
---

Grade: Physiotherapy  
Date: May 13, 2016

## Question 1

Of all the anterior cruciate ligament of the knee injuries, the rupture occurs in 20% of cases, and to detect it there are three different tests:

- The drawer test that analyzes the stability of the tibia. It has a sensitivity of 80% and a specificity of 0.99%.
- A radiologic study in 2 planes, that allows rule out bone avulsion. It has a sensitivity of 0.85% and a specificity of 0.9%.
- A magnetic resonance, that it is the most appropriate when there is hematoma. It has a sensitivity and a specificity of 0.98%.

Assuming that the tests are independent, 

1. Compute the predictive values of the drawer test.
2. If an individual has an anterior cruciate ligament injury, what is the probability that the radiologic study and the magnetic resonance return a positive outcome?
3. If an individual has an anterior cruciate ligament injury, what is the probability that the radiologic study or the magnetic resonance give a wrong diagnosis?

{{< spoiler text="Solution" >}}
1. $PPV_1 = P(D\vert +_1) = 0.9524$ and $NPV_1=P(\bar D\vert -_1)=0.9519$. 
2. $P(+_2)=0.25$, $P(+_3)=0.212$ and $P(+_2\cap +_3)=0.053$.  
3. $P(\mbox{Error}_2)=0.11$, $P(\mbox{Error}_3)=0.02$ and $P(\mbox{Error}_2\cup \mbox{Error}_3)=0.1278$.
{{< /spoiler >}}

## Question 2


It is known that 10% of professional soccer players have a cruciate ligament injury during the league. It is also known that the ligament rupture occurs in 20% of cruciate ligament injuries.
    
1. Calculate the probability that in a team with 20 players more than 3 have a cruciate ligament injury during the league.
2. Calculate the probability that in a league with 200 players more than 3 have a ligament rupture.

{{< spoiler text="Solution" >}}
1. Naming $X$ to the number of players in a team with a cruciate ligament injury, $P(X>3)=0.133$. 
2. Naming $Y$ to the number of players in a league with a ligament rupture, $P(Y>3)= 0.5665$.
{{< /spoiler >}}


## Question 3


In a blood analysis the LDL cholesterol level reference interval for a particular population is $(42,155)$ mg/dl. (The reference interval contains the 95% of the population and is centered in the mean).  
Assuming that the LDL cholesterol level follows a normal distribution, 

1. Calculate the mean and the standard deviation of the LDL cholesterol level.
2. According to the LDL cholesterol level, patients are classified into three categories of infarct risk:

   |LDL cholesterol level     | Infarct risk |
   |:------------------------:|:------------:|
   |Less than 100 mg/dl       | Low          |
   |Between 100 and 160 mg/dl | Medium       |
   |Greater than 160 mg/dl    | High         |
 
   Calculate the percentage of people in the population that falls into every category of infarct risk. 

3. The probability of having an infarct with a high risk is twice the probability of having infarct with a medium risk, and this is twice the probability of having infarct with a low risk. What is the probability of having infart in the whole population if the probability of having infarct with a low risk is 0.01?

{{< spoiler text="Solution" >}}
Naming $C$ to the LDL cholesterol level, 
1. $\mu=98.5$ mg/dl and $\sigma=28.25$ mg/dl. 
2. $P(\mbox{Low})=P(C<100)=0.5199$, $P(\mbox{Medium})=P(100\leq C\leq 160)=0.4654$ and $P(\mbox{Low})=P(C>160)=0.0146$. Thus, there are 51.99% of persons with low risk,  46.54% of persons with medium risk and  1.46% of persons with high risk. 
3. Naming $I$ to the event of havig an infarct, $P(I)=0.0151$.
{{< /spoiler >}}

