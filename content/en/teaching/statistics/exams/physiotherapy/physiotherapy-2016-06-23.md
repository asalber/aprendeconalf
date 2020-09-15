---
title: Physiotherapy exam 2016-06-23
date: 2016-06-23
tags: [Exam, Statistics, Biostatistics]
categories: [Statistics, Biostatistics, Physiotherapy]
type: book
---

Grade: Physiotherapy  
Date: June 23, 2016

## Question 1

It is believed that the age at which a person finish their first marathon depends on gender. 
To check it, a sample of 180 marathon runners was drawn. 
For every runner it was recorded the gender, the age (in years) when they finish the first marathon and if they finish with tendinitis. 
The data are summarized in the table below. 


<table class='data_table' style='border-collapse: collapse; margin-top: 1em; margin-bottom: 1em;' >
<thead>
<tr>
<th style='border-top: 2px solid grey;'></th>
<th colspan='2' style='font-weight: 900; border-bottom: 1px solid grey; border-top: 2px solid grey; text-align: center;'>Males</th><th style='border-top: 2px solid grey;; border-bottom: hidden;'>&nbsp;</th>
<th colspan='2' style='font-weight: 900; border-bottom: 1px solid grey; border-top: 2px solid grey; text-align: center;'>Females</th>
</tr>
<tr>
<th style='font-weight: 900; border-bottom: 1px solid grey; text-align: center;'>Age</th>
<th style='border-bottom: 1px solid grey; text-align: center;'>Finished</th>
<th style='border-bottom: 1px solid grey; text-align: center;'>With tendinitis</th>
<th style='border-bottom: 1px solid grey;' colspan='1'>&nbsp;</th>
<th style='border-bottom: 1px solid grey; text-align: center;'>Finished</th>
<th style='border-bottom: 1px solid grey; text-align: center;'>Width tendinitis</th>
</tr>
</thead>
<tbody>
<tr>
<td style='text-align: left;'>(10,20]</td>
<td style='text-align: right;'>7</td>
<td style='text-align: right;'>2</td>
<td style='' colspan='1'>&nbsp;</td>
<td style='text-align: right;'>3</td>
<td style='text-align: right;'>1</td>
</tr>
<tr>
<td style='text-align: left;'>(20,30]</td>
<td style='text-align: right;'>35</td>
<td style='text-align: right;'>12</td>
<td style='' colspan='1'>&nbsp;</td>
<td style='text-align: right;'>22</td>
<td style='text-align: right;'>5</td>
</tr>
<tr>
<td style='text-align: left;'>(30,40]</td>
<td style='text-align: right;'>30</td>
<td style='text-align: right;'>6</td>
<td style='' colspan='1'>&nbsp;</td>
<td style='text-align: right;'>29</td>
<td style='text-align: right;'>4</td>
</tr>
<tr>
<td style='text-align: left;'>(40,50]</td>
<td style='text-align: right;'>15</td>
<td style='text-align: right;'>2</td>
<td style='' colspan='1'>&nbsp;</td>
<td style='text-align: right;'>22</td>
<td style='text-align: right;'>3</td>
</tr>
<tr>
<td style='text-align: left;'>(50,60]</td>
<td style='text-align: right;'>9</td>
<td style='text-align: right;'>1</td>
<td style='' colspan='1'>&nbsp;</td>
<td style='text-align: right;'>3</td>
<td style='text-align: right;'>0</td>
</tr>
<tr>
<td style='border-bottom: 2px solid grey; text-align: left;'>(60,70]</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>4</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>0</td>
<td style='border-bottom: 2px solid grey;' colspan='1'>&nbsp;</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>1</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>0</td>
</tr>
</tbody>
</table>

1. Calculate the average age at which it is finished the first marathon, both of males and females. Which mean is more representative? Justify the answer. 

2. Calculate the interquartile range of the age for the joint distribution (joining males and females) and interpret it. 

3. What age distribution is more asymmetric, males or females distribution. Justify the answer.

4. Taking into account the relative spread in each group, who finished a marathon before, a man that finished his first marathon at the age of 48 or a woman that finished her first marathon at the age of 47? Justify the answer.

5. Using frequencies to approximate probabilities, compute the following probabilities:

  - Probability that a runner finish their first marathon with tendinitis.
  - Probability that a man 40 or less years old finish their first marathon with tendinitis. 
  - Probability that a woman who finish her first marathon with tendinitis is between 20 and 30 years old. 

Use the following sums for the calculations:
Males: $\sum n_i  = 100$, $\sum x_i n_i = 3460$, $\sum x_i^2 n_i= 134700$, $\sum(x_i-\bar x)^3 n_i =121987$, $\sum(x_i-\bar x)^4 n_i =6480792$
Females: $\sum n_i  = 80$, $\sum x_i n_i = 2830$, $\sum x_i^2 n_i= 107800$, $\sum(x_i-\bar x)^3 n_i =18346$, $\sum(x_i-\bar x)^4 n_i =2175992$


{{< spoiler text="Solution" >}}
1. Males: $\bar x_m = 34.6$ years, $s_m=12.2409$ years, $cv_m=0.3538$. 
Females: $\bar x_f = 35.375$ years, $s_f=9.8035$ years, $cv_f=0.2771$. 
The mean of females is more representative as the coefficient of variation is lower. 
2. $IQR=16.292$ years. The spread of central data is low. 
3. Coeff. of skewness of males $g_{1m}=0.2434$ and coeff. of skewness of females $g_{1f}=0.8378$, thus the males distribution of ages is less asymmetric. 
4. Standard score for a man of 48 years $z_m(48)=1.0947$ and standard score for a woman of 47 years $z_m(47)=1.1858$, thus the man finished his first marathon before. 
5. Naming $T$ to the event of finishing the first marathon with tendinitis, $M$ to the event of being male and $F$ to the event of being female, $P(T)=0.2$, $P(T|M\cap \mbox{Age}<=40) = 0.2778$, $P(\mbox{Age}\in (20,30]|T\cap F) = 0.3846$.
{{< /spoiler >}}

## Question 2 
A study tries to determine if the number of muscular injuries of professional athletes depends on stress. 
The study lasted four years and measured the average level of stress and the number of muscular injuries suffered by a group of athletes.
The collected data is shown in the table below. 

<table class='data_table' style='border-collapse: collapse; margin-top: 1em; margin-bottom: 1em;' >
<tbody>
<tr style='border-top: 2px solid grey;'>
<td style='border-top: 2px solid grey; text-align: left;'>Stress ($X$)</td>
<td style='border-top: 2px solid grey; text-align: right;'>2.3</td>
<td style='border-top: 2px solid grey; text-align: right;'>3.8</td>
<td style='border-top: 2px solid grey; text-align: right;'>5.1</td>
<td style='border-top: 2px solid grey; text-align: right;'>1.4</td>
<td style='border-top: 2px solid grey; text-align: right;'>6.9</td>
<td style='border-top: 2px solid grey; text-align: right;'>7.2</td>
<td style='border-top: 2px solid grey; text-align: right;'>3.2</td>
<td style='border-top: 2px solid grey; text-align: right;'>8.3</td>
</tr>
<tr>
<td style='border-bottom: 2px solid grey; text-align: left;'>Injuries ($Y$)</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>3</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>6</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>7</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>2</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>6</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>8</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>4</td>
<td style='border-bottom: 2px solid grey; text-align: right;'>8</td>
</tr>
</tbody>
</table>


1. Calculate the linear regression model of the number of injuries on stress.

2. According to the most appropriate linear model, what stress level is expected for an athlete that suffered 4 injuries in that period?

3. Calculate the logarithmic regression model of the number of injuries on stress. 

4. Which regression model is better, the linear or the logarithmic? Justify the answer.

Use the following sums for the calculations: $\sum x_i = 38.2$, $\sum y_j=44$, $\sum \log(x_i)=11.3186$, $\sum \log(y_j)=12.8664$, $\sum x_i^2 = 226.28$, $\sum y_j^2=278$, $\sum \log^2(x_i)=18.7028$, $\sum \log^2(y_j)=22.4647$, $\sum x_iy_j = 246.4$, $\sum x_i\log(y_j)=69.2607$, $\sum \log(x_i)y_j=71.5508$, $\sum \log(x_i)\log(y_j)=20.2895$.

{{< spoiler text="Solution" >}}

1. $\bar x=4.775$ points, $s_x^2=5.4844$ points$^2$. 
$\bar y=5.5$ injuries, $s_y^2=4.5$ injuries$^2$. 
$s_{xy}=4.5375$ points$\cdot$injuries. 
Regression line of injuries on stress: $y=1.5494 + 0.8274x$. 

2. $x(4)=3.2625$. 

2. $\overline{\log(x)}=1.4148$ log(points), $s_{\log(x)}^2=0.3361$ log(points)$^2$. 
$s_{\log(x)y}=1.1623$ log(points)$\cdot$injuries. 
Logartihmic model of injuries on stress: $y=0.6075 + 3.458\log(x)$. 
4. Linear coefficient of determination $r^2=0.8342$. 
Logarithmic coefficient of determination $r^2=0.8932$. 
Thus, the logarithmic model fits better.
{{< /spoiler >}}


## Question 3


A diagnostic test with a sensitivity of 96% and a specificity of 93% is used to determine a disease with a prevalence of 10%.

1. What are the positive and negative predictive values of the test?

2. If the test is applied to 15 persons, what is the probability of having more than one positive outcomes?

3. If the test is applied to 50 persons, what is the probability of having a wrong diagnosis in more than two persons?

{{< spoiler text="Solution" >}}
1. $PPV = P(D\vert +) = 0.6038$ and $NPV=P(\bar D\vert -)=0.9952$. 
2. Naming $X$ to the number of positive outcomes after applying the test to a sample of 15 persons, $P(X>1)=0.7144$. 
3. Naming $Y$ to the number of wrong diagnosis after applying the test to a sample of 50 persons, $P(Y>2)=0.6505$.
{{< /spoiler >}}


## Question 4


It is known from previous studies that the hours of study of Statistics for students that pass the subject follows a normal distribution with mean 50 hours and standard deviation unknown; while for students that fail the subject follows a normal distribution with mean unknown and standard deviation 10 hours. If 20% of students that pass study more than 70 hours and 30% of students that fail study less than 25 hours,

1. Calculate the standard deviation of the hours of study distribution for students that pass and the mean of the distribution for students that fail.

2. If a year there are 200 students enrolled in the subject and 150 of them pass, how many of the total students have studied more than 55 hours?

{{< spoiler text="Solution" >}}
Naming $H_p$ and $H_f$ to the number of hours of study for students thar pass and fail respectively, 
1. $\sigma_p=23.7637$ mg/dl and $\mu_f=30.141$ hours. 
2. $62.8244$ students. 
{{< /spoiler >}}

