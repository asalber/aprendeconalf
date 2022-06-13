---
title: Physiotherapy exam 2022-06-06
date: 2022-06-06
tags: [Exam, Statistics, Biostatistics, Physiotherapy]
categories: [Statistics, Biostatistics]
type: book
---

Degrees: Physiotherapy  
Date: June 6, 2022

## Question 1

The patients of a physiotherapy clinic were asked to assess their satisfaction in a scale from 0 to 10. The assessments are summarized in the table below.

$$\begin{array}{lr} 
\hline 
\mbox{Assessment} & \mbox{Patients}\newline
0 - 2 & 3 \newline
2 - 4 & 12 \newline
4 - 6 & 9 \newline
6 - 8 & 18 \newline
8 - 10 & 22 \newline
\hline \end{array}
$$

1. Compute the interquartile range of the assessment and interpret it.

2. If it is required an assessment greater than 5 in more than 50% of patients for the clinic to remain open, will the clinic remain open?

3. Is the assessment mean representative?

4. Compute the coefficient of kurtosis of the assessment and interpret it. Is the kurtosis normal?

5. If the assessment mean of another clinic is 6.8 and the standard deviation is 2.6, which assessment is relatively higher 6 in the first clinic or 6.2 in the second?

Use the following sums for the computations: $\sum x_in_i=408$, $\sum x_i^2n_i=3000$, $\sum (x_i-\bar x)^3n_i=-548.25$ and $\sum (x_i-\bar x)^4n_i=5140.45$.

{{< spoiler text="Show solution" >}}
Let $X$ be the patient assessment.

1. $Q_1= 4.4444$, $Q_3=9.0907$ and $IQR = 4.6463$, so the central dispersion is moderate.

2. $F(5)=0.2695$, and the percentage of patients with an assessment greater than 5 is $73.05\\%$.

3. $\bar x = 6.375$, $s_x^2 = 6.2344$, $s_x=2.4969$ and $cv=0.3917$, thus the representativity of the mean is moderate.

4. $g_2 = -0.9335$ and the distribution is flatter than a Gauss bell, but normal, as $g_2$ is between -2 and 2.

5. First clinic: $z(6)=-0.1502$  
Second clinic: $z(6.2)=-0.3077$.  
Thus, an assessment of 6 in the first clinic is relatively higher as its standard score is greater.
{{< /spoiler >}}

## Question 2

A study tries to determine the effectiveness a training program to increase the grip strength. The table below shows the grip strength in Kg in some weeks of the training program.

$$
\begin{array}{lrrrrrrrr}
\hline
\mbox{Week} & 1 & 3 & 6 & 9 & 14 & 17 & 21 & 24 \newline
\mbox{Grip strength} & 15 & 22 & 29 & 34 & 36 & 39 & 40 & 41 \newline
\hline
\end{array}
$$

1. Compute the regression coefficient of the grip strength on the weeks and interpret it.

2. According to the logarithmic regression model, what is the expected grip strength after 5 and 25 weeks. Are these predictions reliable? Would these predictions be more reliable with the linear regression model?

3. According to the exponential regression model, how many weeks are required to have a grip strength of 25 Kg?

4. What percentage of the total variability of the weeks is explained by the exponential model?

Use the following sums ($X$=Weeks and $Y$=Grip strength):  
$\sum x_i=95$, $\sum \log(x_i)=16.7824$, $\sum y_j=256$, $\sum \log(y_j)=27.3423$,  
$\sum x_i^2=1629$, $\sum \log(x_i)^2=43.606$, $\sum y_j^2=8804$, $\sum \log(y_j)^2=94.3237$,  
$\sum x_iy_j=3552$, $\sum x_i\log(y_j)=342.9642$, $\sum \log(x_i)y_j=608.4186$, $\sum \log(x_i)\log(y_j)=60.047$.


{{< spoiler text="Show solution" >}}
1. $\bar x=11.875$ weeks, $s_x^2=62.6094$ weeks$^2$.  
$\bar y=32$ Kg, $s_y^2=76.5$ Kg$^2$.  
$s_{xy}=64$ weeks$\cdot$Kg.  
Regression coefficient of $Y$ on $X$: $b_{yx} = 1.0222$ Kg/week. The grip strength increases $1.0222$ Kg per week.

2. $\overline{\ln(x)} = 2.0978$ ln(weeks), $s_{\ln(x)}^2 = 1.05$ ln(weeks)$^2$ and $s_{\ln(x)y} = 8.9226$ ln(weeks)Kg.  
Logarithmic regression model of $Y$ on $X$: $y = 14.1729 + 8.498 \ln(x)$.  
Predictions: $y(5) = 27.8499$ Kg and $y(25) = 41.5268$ Kg.  
Logarithmic coefficient of determination: $r^2 = 0.9912$. The predictions are not reliable because the sample size is small.  
Linear coefficient of determination: $r^2 = 0.8552$.  
As the linear coefficient of determination is less than the logarithmic one, the predictions with the logarithmic model are more reliable.

3. Exponential regression model of $X$ on $Y$: $x = e^{-1.6345 + 0.1166y}$.  
Prediction: $x(25)=3.6015$ Weeks.

4. As $r^2 = 0.9912$, the exponential models explains $99.12$% of the variability of the weeks.  
{{< /spoiler >}}

## Question 3

A diagnostic test for a cervical injury has a 99% of sensitivity and produces 80% of right diagnosis. Assuming that the prevalence of the injury is 10%:

1. Compute the specificity of the test.

2. Can we rule out the injury with a negative outcome of the test?

3. Can we diagnose the injury with a positive outcome of the test? What must the minimum prevalence of the injury be to diagnose the injury with a positive outcome of the test?

{{< spoiler text="Show solution" >}}
1. Specificity = $P(-|\overline D) = 0.7789$.

2. Negative predictive value = $P(\overline D|-) = 0.9986 > 0.5$, so we can rule out the injury with a negative outcome.

3. Positive predictive value = $P(D|+) = 0.3322 < 0.5$, so we can not diagnose the injury with a positive outcome. The minimum prevalence required to be able to diagnose the injury with a positive outcome is $P(D)=0.1825$.
{{< /spoiler >}}

## Question 4

A pharmacy sells two vaccines $A$ and $B$ against a virus. The $A$ vaccine produces 5% of side effects, while the $B$ vaccine produces 2% of side effects. The pharmacy has sold 10 units of the $A$ vaccine and 100 units of the $B$ vaccine.

1. Compute the probability of having less than 2 side effects with the $A$ vaccine.

2. Compute the probability of having more than 3 side effects with the $B$ vaccine.

3. If we apply both vaccines to the same person at different moments, and assuming that the production of side effects of the vaccines are independent, what is the probability that this person will have any side effect?

{{< spoiler text="Show solution" >}}
1. Let $X$ be the number of side effects in 10 applications of A vaccine. Then, $X\sim B(10, 0.05)$ and $P(X<2) = 0.9139$.

2. Let $Y$ be the number of side effects in 100 applications of B vaccine. Then, $Y\sim B(100, 0.02)\approx P(2)$ and $P(Y>3) = 0.1429$.

3. Let $A$ and $B$ the events of having side effects with vaccines A and B respectively. $P(A\cup B) = 0.069$.
{{< /spoiler >}}

## Question 5

The length of the femur bone is normally distributed in both men and women with a standard deviation of 4 cm. It is also known that the first quartile in women is 42.3 cm, while the third quartile in men is 50.7 cm.

1. What is the difference between the means of the femur length of women and men?  
Remark: If you do not know how to compute the means, use a mean 44 cm for women and a mean 47 cm for men in the following parts.

2. Compute the 60th percentile of the femur length in women. What percentage of men have a femur length less than the 60th percentile of women?

3. If we pick a woman and man at random, what is the probability that neither of them has a femur length less than 45 cm?

{{< spoiler text="Show solution" >}}
Let $X$ and $Y$ be the femur length of women and men respectively. Then $X\sim N(\mu_x, 4)$ and $Y\sim N(\mu_y,4)$.

1. $\mu_x = 44.91$ cm, $\mu_y = 48.02$ cm and $\mu_x - \mu_y = -3.11$ cm.

2. 60th percentile in women $P_{60}=45.9234$ cm, and $P(Y<45.9234) = 0.3001$, that is, a $30.01\\%$ of men have a femur length less than the 60th percentile of women.

3. $P(X\geq 45 \cap Y\geq 45) = 0.3805$. 
{{< /spoiler >}}