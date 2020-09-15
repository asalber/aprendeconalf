---
title: Problems of Probability
linkTitle: Probability
date:
lastmod: 
tags: [Probability]
categories: [Statistics, Biostatistics]
type: book
weight: 50
---

## Exercise 1

Construct the sample space of the following random experiments:

1.  Pick a random person and record the gender and whether she or he is smoker or not.
2.  Pick a random person and record the blood type and whether she or he is smoker or not.
3.  Pick a random person and record the gender, the blood type and whether she or he is smoker or not.


## Exercise 2 
There are two boxes with balls of different colors. The first box contains 3 white balls and 2 black balls, and the second one contains 2 blue balls, 1 red ball and 1 green ball. Construct the sample space of the following random experiments:

1.  Pick a random ball from every box.
2.  Pick two random balls from every box.

## Exercise 3
The Morgan’s laws state that given two events $A$ and $B$ from the same sample space, $\overline{A\cup B}=\bar A \cap \bar B$ and $\overline{A\cap B}=\bar A \cup \bar B$. Proof both statements graphically using Venn diagrams.

## Exercise 4
Compute the probability of the following events of the random experiment consisting in tossing 3 coins:

1.  Get exactly 1 head.
2.  Get exactly 2 tails.
3.  Get two or more heads.
4.  Get some tails.

{{< spoiler text="Solution" >}}
1. $P(\mbox{1 head})=0.375$.  
2. $P(\mbox{2 tails})=0.375$.  
3. $P(\mbox{2 or more heads})=0.5$.  
4. $P(\mbox{some tails})=0.875$.
{{< /spoiler >}}

## Exercise 5
In a laboratory there are 4 flasks with sulfuric acid and 2 with nitric acid, and in another laboratory there are 1 flask with sulfuric acid and 3 with nitric acid. A random experiment consist in picking two flask, one from every laboratory. Compute the probability of the following events:

1.  The two picked flasks are of sulfuric acid.
2.  The two picked flasks are of nitric acid.
3.  The two picked flasks contains different acids.

Compute again the above probabilities if the flask picked in the first laboratory is put in the second laboratory before picking the flask from it.

{{< spoiler text="Solution" >}}
1. $P(\mbox{Two flasks of sulfuric acid})=4/24$.<br/>
2. $P(\mbox{Two flasks of nitric acid})=6/24$.<br/>
3. $P(\mbox{One flask  of each})=14/24$.<br/>
Putting the first flask in the second laboratory:<br/>
1. $P(\mbox{Two flasks of sulfuric acid})=8/30$.<br/>
2. $P(\mbox{Two flasks of nitric acid})=8/30$.<br/>
3. $P(\mbox{One flask  of each})=14/30$.
{{< /spoiler >}} 

## Exercise 6
Let $A$ and $B$ two be events of a same sample space, such that $P(A)=3/8$, $P(B)=1/2$, $P(A\cap B)=1/4$. Compute the following probabilities:

1.  $P(A\cup B)$.
2.  $P(\bar A)$ y $P(\bar B)$.
3.  $P(\bar A\cap \bar B)$.
4.  $P(A\cap \bar B)$.
5.  $P(A\vert B)$.
6.  $P(A\vert \bar B)$.

{{< spoiler text="Solution" >}}
1. $P(A\cup B)=5/8$.<br/>
2. $P(\bar A)=5/8$ and $P(\bar B)=1/2$.<br/>
3. $P(\bar A\cap \bar B)=3/8$.<br/>
4. $P(A\cap \bar B)=1/8$.<br/>
5. $P(A\vert B)=1/2$.<br/>
6. $P(A\vert \bar B)=1/4$.<br/>
{{< /spoiler >}}

## Exercise 7
In a hospital the probability of getting hepatitis in a blood transfusion from a unit of blood is $0.01$. A patient gets two units of blood while staying at the hospital. What is the probability of getting hepatitis?

{{< spoiler text="Solution" >}}
$P(\mbox{Hepatitis})=0.0199$.
{{< /spoiler >}}

## Exercise 8
Let $A$ and $B$ be two events of a same sample space, such that $P(A)=0.6$ and $P(A\cup B)=0.9.$ Compute $P(B)$ under the following assumptions:

1.  $A$ and $B$ are incompatible.
2.  $A$ and $B$ are independent.

{{< spoiler text="Solution" >}}
1. $P(B)=0.3$.<br/>
2. $P(B)=0.75$.
{{< /spoiler >}}

## Exercise 9
A study about smoking has found that 40% of smokers have a smoker father, 25% have a smoker mother and 52% have al least one of the parents smoker. We pick a random person from this population. Answer the following questions:

1.  What is the probability of having a smoker mother if the father smokes?
2.  What is the probability of having a smoker mother if the father does not smoke?
3.  Are independent the events having a smoker father and having a smoker mother?

{{< spoiler text="Solution" >}}
Naming $SF$ tho the event of having a smoker father and $SM$ to the event of having a smoker mother,  
1. $P(SM/SF)=0.325$.  
2. $P(SM/\bar SF)=0.2$.  
3. The events aren't independent.  
{{< /spoiler >}}

## Exercise 10
The probability that an injury $A$ is repeated is $4/5$, the probability that another injury $B$ is repeated is $1/2$, and the probability that both injuries are repeated is $1/3$. Compute the probability of the following events:

1.  Only injury $B$ is repeated.
2.  At least one injury is repeated.
3.  Injury $B$ is repeated if injury $A$ has been repeated.
4.  Injury $B$ is repeated if injury $A$ has not been repeated.

{{< spoiler text="Solution" >}}
1. $P(B\cap\overline A)=1/6$.  
2. $P(A\cup B)=29/30$.  
3. $P(B\vert A)=5/12$.  
4. $P(B\vert \overline A)=5/6$.
{{< /spoiler >}}

## Exercise 11
In a digestive clinic, from every 1000 patients that arrive with stomach pain, 700 have gastritis, 200 have an ulcer and 100 have cancer. After analyzing the gastric symptoms, it is known that the probability of vomiting is $0.3$ in case of gastritis, $0.6$ in case of ulcer and $0.9$ in case of cancer. What is the diagnosis for a new patient with stomach pain that suffers from vomiting?

Note: Assume that the only diseases are gastritis, ulcer and cancer and that are incompatible among them.

{{< spoiler text="Solution" >}}
Let $G$, $U$ and $C$ be the events of having gastritis, ulcer and cander respectively, and let $V$ be the event of vomiting, $P(G/V)=0.5$, $P(U/V)=0.286$ and $P(C/V)=0.214$, so, the diagnosis is gastritis.
{{< /spoiler >}}


## Exercise 12


A severe pain without effusion in a particular zone of the knee joint is a symptom of sprained lateral collateral ligament (SLCL). If the sprains in that ligament are classified into grade 1, when there is only distension (60% of cases), grade 2 when there is a partial tearing (30% of cases) and grade 3 when there is a complete tearing (10% of cases). Taking into account that the symptom appears in 80% of cases of grade 1 sprains, 90% of cases of grade 2 and 100% of cases of grade 3, answer the following questions:

1.  If a person has SLCL what is the probability that he or she present severe pain without effusion?
2.  What is the diagnosis for a person with severe pain without effusion?
3.  From a total of 10000 people with severe pain without effusion, how many are expected to have a grade 1 sprain? How many are expected to have a grade 2 sprain? And a grade 3 sprain?

{{< spoiler text="Solution" >}}
Naming $S$ to the event of presenting severe pain without effusion, and $G1$, $G2$ and $G3$ to the events of having a SLCL of grade 1, 2 and 3 respectively,  
1. $P(S)=0.85$.  
2. $P(G1\vert S)=0.5647$, $P(G2\vert S)=0.3176$ and $P(G3\vert S)=0.1176$, so the diagnosis is a SLCL of grade 1.  
3. $5647.0588$ will have a grade 1 sprain, $3176.4706$ will have a grade 2 sprain and $1176.4706$ will have a grade 3 sprain.
{{< /spoiler >}}


## Exercise 13
A physiotherapist uses two techniques $A$ and $B$ to cure an injury. It is known that the injury is 3 times more frequent in people over 30 than in people under 30. It is also known that in people over 30 technique $A$ works in 30% of cases and technique $B$ in 60%, while in people under 30 technique $A$ works in 50% of cases and technique $B$ in 70%. If both techniques are applied with the same probability, no matter the age,

1.  What is the probability that a random person under 30 is cured? And for a people over 30?
2.  What is the probability that a random person is cured?
3.  If after applying a technique to a person over 30, the person does not cure, what is the probability that the technique applied was $A$?

{{< spoiler text="Solution" >}}
Naming $J$ to the event of being under 30, $C$ to the event of being cured, and $A$ and $B$ to the events of applying techniques $A$ and $B$ respectively,  
$P(C\vert J)=0.45.$ and $P(C\vert \bar J)=0.6$. <br />
$P(C)=0.5625$.  
$P(A/\bar J\cap \bar C)=0.625$.
{{< /spoiler >}}
