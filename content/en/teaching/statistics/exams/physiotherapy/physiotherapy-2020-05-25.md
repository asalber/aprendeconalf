---
title: Physiotherapy exam 2020-05-25
date: 2020-05-25
tags: [Exam, Statistics, Biostatistics]
categories: [Statistics, Biostatistics, Physiotherapy]
type: book
---

Degrees: Physiotherapy  
Date: May 25, 2020

# Descriptive Statistics and Regression

## Question 1

In a course there are 150 students, of which 50 are working students and the other 100 non-working students. The table below shows the frequency distribution of the grade in an exam of these two groups:

$$
\begin{array}{crr}
\mbox{Grade} & \mbox{Num non-working students} & \mbox{Num working students} \newline
\hline
0-2 & 8 & 2 \newline
2-4 & 15 & 9 \newline
4-6 & 25 & 19 \newline
6-8 & 38 & 11 \newline
8-10 & 14 & 9 \newline
\hline
\end{array}
$$

1. Compute the percentage of students that passed the exam (a grade 5 or above) in both groups, working and non-working students.

2. In which group is there a higher relative dispersion of the grade with respect to the mean?

3. Which grade distribution is more asymmetric, the distribution of working students, or the non-working students one?

4. To apply for a scholarship to go abroad, the grade must be transformed applying the linear transformation $Y = 0.5 + X *
1.45$. Compute the mean of Y for the two groups. How changes the asymmetry of the two groups?

5. Which grade is relatively higher, 6 in the working students group, or 7 in the non-working students group?

Use the following sums for the computations:  
Non-working students: $\sum x_in_i=570$, $\sum x_i^2n_i=3764$, $\sum (x_i-\bar x)^3n_i=-547.8$ and $\sum (x_i-\bar x)^4n_i=6475.73$.  
Working students: $\sum y_in_i=282$, $\sum y_i^2n_i=1826$, $\sum (y_i-\bar y)^3n_i=-1.31$ and $\sum (y_i-\bar y)^4n_i=2552.14$.

{{< spoiler text="Solution" >}}
1. 35.5% of non-working students passed and 41% of working students passed.
2. Non-working students: $\bar x=5.7$, $s^2=5.15$, $s=2.2694$ and $cv=0.3981$.
Working students: $\bar y=5.64$, $s^2=4.7104$, $s=2.1703$ and $cv=0.3848$.
The sample of non-working students has a slightly higher relative dispersion with respect to the mean as the coefficient of variation is greater.
3.  Non-working students: $g_1=-0.4687$.
Working students: $g_1=-0.0026$.
Thus, the sample of non-working students is more asymmetric as the coefficient os skewness is further from 0.
4.  Non-working students: $\bar y=8.765$.
Working students: $\bar x=8.678$.
The coefficient of skewness does not change as the slope of the linear transformation is positive.
5.  Non-working students: $z(7)=0.5728$.
Working students: $z(6)=0.1659$.
Thus, a 7 in the sample of non-working students is relatively higher than than a 6 in the sample of working students, as its
standard score is greater.
{{< /spoiler >}}

## Question 2

The effect of a doping substance on the response time to a given stimulus was analyzed in a group of patients. The same amount of
substance was administered in successive doses, from 10 to 80 mg, to all the patients. The table below shows the average response time to the stimulus, expressed in hundredths of a second:

$$
\begin{array}{lrrrrrrrr}
\hline
\mbox{Dose (mg)} & 10 & 20 & 30 & 40 & 50 & 60 & 70 & 80 \newline 
\mbox{Response time ($10^{-2}$ s)} & 28 & 46 & 62 & 81 & 100 & 132 & 195 & 302 \newline 
\hline
\end{array}
$$

1. According to the linear regression model, how much will the response time increase or decrease for each mg we increase the
dose?

2. Based on the exponential model, what will be the expected response time for a 75 mg dose?

3. If a response time greater than one second is considered dangerous for health, from what level should the administration of the doping substance be regulated, or even prohibited, according to the logarithmic model?

Use the following sums for the computations:  
$\sum x_i=360$ mg, $\sum \log(x_i)=29.0253$ $\log(\mbox{mg})$, $\sum y_j=946$ $10^{-2}$ s, $\sum \log(y_j)=36.1538$ $\log(\mbox{$10^{-2}$ s})$,  
$\sum x_i^2=20400$ mg$^2$, $\sum \log(x_i)^2=108.7717$ $\log(\mbox{mg})^2$, $\sum y_j^2=169958$ $10^{-2}$ s$^2$, $\sum \log(y_j)^2=167.5694$ $\log(\mbox{$10^{-2}$ s})^2$,  
$\sum x_iy_j=57030$ mg$\cdot 10^{-2}$ s, $\sum x_i\log(y_j)=1758.6576$ mg$\cdot\log(\mbox{$10^{-2}$ s})$, $\sum \log(x_i)y_j=3795.4339$ $\log(\mbox{mg})10^{-2}$ s, $\sum \log(x_i)\log(y_j)=134.823$ $\log(\mbox{mg})\log(\mbox{$10^{-2}$ s})$.

{{< spoiler text="Solution" >}}
1. $\bar x=45$ mg, $s_x^2=525$ mg$^2$.
$\bar y=118.25$ $10^{-2}$ s, $s_y^2=7261.6875$ $10^{-4}$ s$^2$.
$s_{xy}=1807.5$ mg$\cdot 10^{-2}$ s.
$b_{yx} = 3.4429$ $10^{-2}$ s/mg.
Therefore, the response time increases $3.4429$ hundredths of a second for each mg the dose is increased.
2. $\overline{\log(y)}=4.5192$ log($10^{-2}$ s), $s_{\log(y)}^2=0.5227$ log($10^{-2}$ s)$^2$.
$s_{x\log(y)}=16.4669$ mg$\cdot\log(10^{-2}$ s).
Exponential regression model: $y=e^{3.1078+0.0314x}$.
Prediction: $y(75)=235.1434$ $10^{-2}$ s.
Exponential coefficient of determination: $r^2=0.988$
Thus, the exponential model fits almost perfectly to the cloud of points of the scatter plot, but the sample is too small to
get reliable predictions.
3. Logarithmic regression model: $x=-97.3603+31.501\ln(y)$.
Prediction: $x(100)=47.7072$ mg.
{{< /spoiler >}}

# Probability and Random Variables

## Question 3
A hospital orders a DNA compatibility test to three labs A, B and C.
Lab A performs 40 test a day, lab B 50, and lab C 60. It is known
that the probability of a wrong diagnose is 20% in lab A, 18% in lab
B and 22% in lab C. If we select a random test of the hospital,

1. Compute the probability of wrong diagnose in that test.

2. If the test is wrong, what is the probability that it has been performed by lab B?

3. If the test is right, which lab is more likely to have performed the test?

{{< spoiler text="Solution" >}}
Let $A$, $B$ and $C$ be the events of performing the test in labs $A$, $B$ and $C$ respectively, and $R$ the event of getting a right diagnose. According to the statement $P(A)=0.2667$, $P(B)=0.3333$, $P(C)=0.4$, $P(R|A)=0.8$, $P(R|B)=0.82$ and $P(R|C)=0.78$.
1. $P(\overline R) = 0.2013$.
2. $P(B|\overline R) = 0.298$.
3. $P(A|R) = 0.2671$, $P(B|R) = 0.3422$ and $P(C|R) = 0.3907$, thus, it is more likely that it has been performed in lab $C$.
{{< /spoiler >}}

## Question 4

An epidemiological study tries to determine the effectiveness of face masks to prevent the COVID19. In a sample 4000 persons without the virus and 1000 persons with it were selected. I was observed that in the group of infected people 120 had used face masks in the two previous weeks, while in the non-infected group, 1250 had used face masks in the two previous weeks.

1. Compute the relative risk of been infected with face masks.

2. Compute the odds ratio of been infected with face masks.

3. Which association measure is more reliable?

{{< spoiler text="Solution" >}}
Let $D$ be the event of being infected.
1. $RR(D)=0.3613$. Thus, the risk of being infected with face mask is almost one third of the likelihood of been infected without
face mask.
2. $OR(D)=0.3$. Thus, the odds of being infected with face mask is less than one third of the likelihood of been infected without
face mask.
3. As we can not compute the prevalence of $D$, the odds ratio is more reliable.
{{< /spoiler >}}

## Question 5

During the COVID19 quarantine a telephone exchange with 4 telephone operators received an average of 12 calls per day. Assuming that the calls are equally distributed among the operators,

1. Compute the probability that an operator received more than 3 calls a day.

2. Compute the probability that all the the operators received some call a day.

{{< spoiler text="Solution" >}}
1. Let $X$ be the number of calls that arrive to one operator, then $X\sim P(3)$, and $P(X>3)=0.3528$.
2. Let $Y$ be the number of operators that receive some call, then $Y\sim B(4, 0.9502)$, and $P(Y=4)=0.8152$.
{{< /spoiler >}}

## Question 6

In a course with 200 students the score of a test to measure the intelligence quotient follows a normal distribution. After applying the test to the students 10 of them got a score above 130 and 30 of them a score below 60.

1. Compute the mean and the standard deviation of the score.

2. How many students will have a score between 90 and 95?

3. Compute the limits of the interval centered at the mean that accumulates 95% of the scores.

{{< spoiler text="Solution" >}}
1. Let $X$ be the score of the test then $X\sim N(87.058, 26.1069)$
2. $P(90\leq X \leq 95) = 0.0747$, that is, around $14.9309$ students.
3. Interval with 95% of probability $(35.8895, 138.2265)$.
{{< /spoiler >}}
