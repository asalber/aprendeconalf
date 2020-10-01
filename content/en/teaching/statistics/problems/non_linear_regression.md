---
title: Problems of Non Linear Regression
linkTitle: Non Linear Regression
date:
lastmod:
tags: [Regression, Non-linear Regression]
categories: [Statistics, Biostatistics]
type: book
weight: 40
---

## Exercise 1

A dietary center is testing a new diet in sample of 12 persons. The data below are the number of days of diet and the weight loss (in kg) until them for every person.

```
(33,3.9)  (51,5.9)  (30,3.2)  (55,6)  (38,4.9)  (62,6.2)  (35,4.5)  (60,6.1)  (44,5.6)  (69,6.2)  (47,5.8)  (40,5.3) 
```

1. Draw the scatter plot. According to the point cloud, what type of regression model explains better the relation between the weight loss and the days of diet?
2. Construct the linear regression model and the logarithmic regression model of the weight loss on the number of days of diet.
3. Use the best model to predict the weight that will lose a person after 40 and 100 days of diet. Are these predictions reliable?

Use the following sums ($X$=days of diet and $Y$=weight loss):
$\sum x_i=564$ days, $\sum \log(x_i)=45.8086$ $\log(\mbox{days})$, $\sum y_j=63.6$ kg, $\sum x_i^2=28234$ days$^2$, $\sum \log(x_i)^2=175.6603$ $\log(\mbox{days})^2$, $\sum y_j^2=347.7$ kg$^2$, $\sum x_iy_j=3108.5$ days$\cdot$kg, $\sum \log(x_i)y_j=245.4738$ $\log(\mbox{days})\cdot$kg.

{{< spoiler text="Solution" >}}
1.
<img src="../img/diet_scatterplot-1.svg" title="plot of chunk diet_scatterplot" alt="plot of chunk diet_scatterplot" style="display: block; margin: auto;" />
2. Linear model<br/>
$\bar x=47$ days, $s_x^2=143.8333$ days$^2$.<br/>
$\bar y=5.3$ kg, $s_y^2=0.885$ kg$^2$.<br/>
$s_{xy}=9.9417$ days$\cdot$kg.<br/>
Regression line of weight loss on days of diet: $y=2.0514 + 0.0691x$.<br/>
$r^2=0.7765$.<br/>

Logartihmic model<br/>
$\overline{\log(x)}=3.8174$ log(days), $s_{\log(x)}^2=0.0659$ log(days)$^2$.<br/>
$s_{\log(x)y}=0.224$ log(days)$\cdot$kg.<br/>
Logartihmic model of weight loss on days of diet: $y=-7.6678 + 3.397\log(x)$.<br/>
$r^2=0.8599$.<br/>
3. $y(40)=4.8635$ kg and $y(100)=7.9761$ kg. The predictions are reliable because the coefficient of determination is close to 1, but the last one is less reiable as 100 is far from the observed range of values in the sample. 
{{< /spoiler >}}

## Exercise 2
The concentration of a drug in blood, in mg/dl, depends on time, in hours, according to the data below.

$$
\begin{array}{lrrrrrrr}
\hline
\mbox{Time} & 2 & 3 & 4 & 5 & 6 & 7 & 8\newline
\mbox{Drug concentration} & 25 & 36 & 48 & 64 & 86 & 114 & 168\newline
\hline
\end{array}
$$

1. Construct the linear regression model of drug concentration on time.
2. Construct the exponential regression model of drug concentration on time.
3. Use the best regression model to predict the drug concentration after $4.8$ hours? Is this prediction reliable? Justify your answer.

Use the following sums ($C$=Drug concentration and $T$=time): $\sum t_i=35$ h, $\sum \log(t_i)=10.6046$ $\log(\mbox{h})$, $\sum c_j=541$ mg/dl, $\sum \log(c_j)= 29.147$ $\log(\mbox{mg/dl})$, $\sum t_i^2=203$ h$^2$, $\sum \log(t_i)^2=17.5206$ $\log(\mbox{h})^2$, $\sum c_j^2=56937$ (mg/dl)$^2$, $\sum \log(c_j)^2=124.0131$ $\log(\mbox{mg/dl})^2$, $\sum t_ic_j=3328$ h$\cdot$mg/dl, $\sum t_i\log(c_j)=154.3387$ h$\cdot\log(\mbox{mg/dl})$, $\sum \log(t_i)c_j=951.6961$ $\log(\mbox{h})\cdot$mg/dl, $\sum\log(t_i)\log(c_j)=46.08046$ $\log(\mbox{h})\cdot\log(\mbox{mg/dl})$.

{{< spoiler text="Solution" >}}
1. $\bar x=5$ hours, $s_x^2=4$ hours$^2$.<br/>
$\bar y=77.2857$ mg/dl, $s_y^2=2160.7755$ (mg/dl)$^2$.<br/>
$s_{xy}=89$ hours$\cdot$mg/dl.<br/>
Regression line of drug concentration on time: $y=-33.9643 + 22.25x$.<br/>
$r^2=0.9165$.<br/>
2.

$\overline{\log(y)}=4.1639$ log(mg/dl), $s_{\log(y)}^2=0.3785$ log(mg/dl)$^2$.<br/>
$s_{x\log(y)}=1.2291$ hours$\cdot$log(mg/dl).<br/>
Exponential model of drug concentration on time: $y=e^{2.6275 + 0.3073x}$.<br/>
$r^2=0.9979$.<br/>
3. $y(4.8)=60.4853$ mg/dl. 
{{< /spoiler >}}

## Exercise 3
A researcher is studying the relation between the obesity and the response to pain. The obesity is measured as the percentage over the ideal weight, and the response to pain as the nociceptive flexion pain threshold. The results of the study appears in the table below.

$$
\begin{array}{lrrrrrrrrrr}
\hline
\mbox{Obesity} & 89 & 90 & 77 & 30 & 51 & 75 & 62 & 45 & 90 & 20\newline
\mbox{Pain threshold} & 10 & 12 & 11.5 & 4.5 & 5.5 & 7 & 9 & 8 & 15 & 3\newline
\hline
\end{array}
$$




1. According to the scatter plot, what model explains better the relation of the response to pain on the obesity?
2. According to the best regression model, what is the response to pain expected for a person with an obesity of 50%? Is this prection reliable?
3. According to the best regression model, what is the expected obesity for a person with a pain threshold of 10? Is this prediction reliable?

Use the following sums ($X$=Obesity and $Y$=Pain threshold):
$\sum x_i=629$, $\sum \log(x_i)=40.4121$, $\sum y_j=92.2$, $\sum \log(y_j)=21.339$, $\sum x_i^2=45445$, $\sum \log(x_i)^2=165.6795$, $\sum y_j^2=960.14$, $\sum \log(y_j)^2=47.6231$, $\sum x_iy_j=6537.7$, $\sum x_i\log(y_j)=1443.1275$, $\sum \log(x_i)y_j=387.5728$, $\sum \log(x_i)\log(y_j)=88.3696$.

{{< spoiler text="Solution" >}}
1.
<img src="../img/obesity_pain_scatterplot-1.svg" title="plot of chunk obesity_pain_scatterplot" alt="plot of chunk obesity_pain_scatterplot" style="display: block; margin: auto;" />
2. Linear model<br/>
$\bar x=62.9$, $s_x^2=588.09$.<br/>
$\bar y=9.22$, $s_y^2=11.0056$.<br/>
$s_{xy}=82.0356$.<br/>
Regression line of pain threshold on obesity: $y=1.3232 + 0.1255x$.<br/>
$r^2=0.8422$.

Logartihmic model<br/>
$\overline{\log(x)}=4.0412$, $s_{\log(x)}^2=0.2366$.<br/>
$s_{\log(x)y}=1.4973$.<br/>
Logartihmic model of pain threshold on obesity: $y=-16.3578 + 6.3293\log(x)$.<br/>
$r^2=0.8611$.<br/>
$y(50)=8.4023$.<br/>
3. 

Exponential model of obesity on pain threshold: $x=e^{2.7868 + 0.1361y}$.<br/>
$x(10)=63.2648$. 
{{< /spoiler >}}


## Exercise 4
A blood bank keeps plasma at a temperature of 0ºF.
When it is required for a blood transfusion, it is heated in an oven at a constant temperature of 120ºF.
In an experiment it has been measured the temperature of plasma at different times during the heating. 
The results are in the table below.

$$
\begin{array}{lrrrrrrrr}
\hline
\mbox{Time (min)}	& 5 & 8 & 15 & 25 & 30 & 37 & 45 & 60\newline
\mbox{Temperature (ºF)} & 25 & 50 & 86 & 102 & 110 & 114 & 118 & 120\newline
\hline
\end{array}
$$



1. Plot the scatter plot. 
Which type of regression model do you think explains better relationship between temperature and time?
2. Which transformation should we apply to the variables to have a linear relationship?
3. Compute the logarithmic regression of the temperature on time.
4. According to the logarithmic model, what will the temperature of the plasma be after 15 minutes of heating?
Is this prediction reliable? Justify your answer.

Use the following sums ($X$=Time and $Y$=Temperature):
$\sum x_i=225$ min, $\sum \log(x_i)=24.5289$ log(min), $\sum y_j=725$ ºF, $\sum \log(y_j)=35.2051$ log(ºF), $\sum x_i^2=8833$ min², $\sum \log(x_i)^2=80.4703$ log²(min), $\sum y_j^2=74345$ ºF², $\sum \log(y_j)^2=157.1023$ log²(ºF), $\sum x_iy_j=24393$ min⋅ºF, $\sum x_i\log(y_j)=1048.0142$ min⋅log(ºF), $\sum \log(x_i)y_j=2431.7096$ log(min)⋅ºF, $\sum \log(x_i)\log(y_j)=111.1165$ log(min)log(ºF).

{{< spoiler text="Solution" >}}
1. 
<img src="../img/temperature_time_scatterplot-1.svg" title="plot of chunk temperature_time_scatterplot" alt="plot of chunk temperature_time_scatterplot" style="display: block; margin: auto;" />
A logarithmic model.<br/>
2. Apply a logarithmic transformation to time $z=\log(x)$.  

3. $\bar z=28.125$ log(min), $s_z^2=0.6577$ log²(min).<br/>
$\bar y=90.625$ ºF, $s_y^2=1080.2344$ ºF².<br/>
$s_{zy}=26.0969$ log(min)ºF.<br/>
Logarithmic model of temperature on time: $y=-31.0325 + 39.6781\log(x)$.<br/>
4. $y(15)=76.4176$ ºF.<br/>
$r^2=0.9586$, that is close to 1, so the prediction is reliable.
{{< /spoiler >}}


## Exercise 5
The activity of a radioactive substance depends on time according to the data in the table below.

$$
\begin{array}{lrrrrrrrr}
\hline
t\mbox{ (hours)} & 0 & 10 & 20 & 30 & 40 & 50 & 60 & 70 \newline
A\mbox{ ($10^7$ disintegrations/s)} & 25.9 & 8.16 & 2.57 & 0.81 & 0.25 & 0.08 & 0.03 & 0.01\newline
\hline
\end{array}
$$



1. Represent graphically the data of radioactivity as a function of time.
Which type of regression model explains better the relationship between radioactivity and time?
2. Represent graphically the data of radioactivity as a function of time in a semi-logarithmic paper.
3. Compute the regression line of the logarithm of radioactivity on time.
4. Taking into account that radioactivity decay follows the formula
\newline[
A(t) = A_0 e^{-\lambda t}
\newline]
where $A_0$ is the number of disintegrations at the begining and $\lambda$ is a disintegration constant, different for each radioactive substance, use the slope of the previous regression line to compute the disintegration constant for the substance. 

Use the following sums ($X$=Time and $Y$=Radioactivity):
$\sum x_i=280$ hours, $\sum y_j=37.81$ 10⁷ disintegrations/s, $\sum \log(y_j)=-5.9371$ log(10⁷ disintegrations/s), $\sum x_i^2=14000$ hours², $\sum y_j^2=744.7265$ 10⁷ disintegrations/s², $\sum \log(y_j)^2=57.7369$ log²(10⁷ disintegrations/s), $\sum x_iy_j=173.8$ hours⋅10⁷ disintegrations/s, $\sum x_i\log(y_j)=-680.9447$ hours⋅log(10⁷ disintegrations/s).

{{< spoiler text="Solution" >}}
1. 
<img src="../img/radioactivity_time_scatterplot-1.svg" title="plot of chunk radioactivity_time_scatterplot" alt="plot of chunk radioactivity_time_scatterplot" style="display: block; margin: auto;" />
2. 
<img src="../img/log_radioactivity_time_scatterplot-1.svg" title="plot of chunk log_radioactivity_time_scatterplot" alt="plot of chunk log_radioactivity_time_scatterplot" style="display: block; margin: auto;" />

3. $\bar x=35$ hours, $s_x^2=525$ hours².<br/>
$\bar z=-0.7421$ log(10⁷ disintegrations/s), $s_z^2=6.6664$ log(10⁷ disintegrations/s)^2.<br/>
$s_{xz}=-59.1434$ hours⋅log(10⁷ disintegrations/s)<br/>
Regression line of logarithm of radioactivity on time: $z=3.2008 + -0.1127x$.<br/>
4. $\lambda=0.1127$.
{{< /spoiler >}}

## Exercise 6
For oscillations of small amplitude, the oscillation period $T$ of a pendulum is given by the formula
\newline[
T = 2\pi\sqrt{\frac{L}{g}}
\newline]
where $L$ is the length of the pendulum and $g$ is the gravitational constant. In order to check if the previous formula is satisfied, an experiment has been conducted where it has been measured the oscillation period for different lengths of the pendulum.The measurements are shown in the table below.

$$
\begin{array}{lrrrrr}
\hline
L\text{ (cm)} & 52.5 & 68.0 & 99.0 & 116.0 & 146.0 \newline
P\text{ (seg)} & 1.449 & 1.639 & 1.999 & 2.153 & 2.408\newline
\hline
\end{array}
$$



1. Represent graphically the data of the period versus the length of the pendulum.  
Does a linear model fit well to the points cloud?
2. Represent graphically the data of the period versus the length in a logarithmic paper.
Which type of model fits better to the points cloud?
3. Compute the regression line of the logarithm of period on the logarithm of length.
4. Taking in to account the independent term of the previous regression line, compute the value of $g$.

{{< spoiler text="Solution" >}}
1. 
<img src="../img/period_length_scatterplot-1.svg" title="plot of chunk period_length_scatterplot" alt="plot of chunk period_length_scatterplot" style="display: block; margin: auto;" />
The linear model fits well to the points cloud.  
<img src="../img/log_period_length_scatterplot-1.svg" title="plot of chunk log_period_length_scatterplot" alt="plot of chunk log_period_length_scatterplot" style="display: block; margin: auto;" />
2. The model that best fits the points cloud is linear.  
3. Let $X$ be the logarithm of length and $Y$ to the logarithm of period,  

$\bar x=4.5025$ log(cm), $s_x^2=0.1353$ log(cm)².<br/>
$\bar y=0.6407$ log(s), $s_y^2=0.0339$ log(s)².<br/>
$s_{xy}=0.0677$ log(cm)log(s)  
Regression line of Y on X: $y=-1.6132 + 0.5006x$.<br/>
4. $g=994.4579 cm/s². 
{{< /spoiler >}}
  
## Exercise 7
A study tries to determine the relationship between two substances $X$ and $Y$ in blood.
The concentrations of these substances have been measured in seven individuals (in $\mu$g/dl) and the results are shown in the table below. 

$$
\begin{array}{rrrrrrrr}
\hline
X & 2.1 & 4.9 & 9.8 & 11.7 & 5.9 & 8.4 & 9.2 \newline 
Y & 1.3 & 1.5 & 1.7 & 1.8 & 1.5 & 1.7 & 1.7 \newline 
\hline
\end{array}
$$



1. Are $Y$ and $X$ linearly related?
2. Are $Y$ and $X$ potentially related?
3. Use the best of the previous regression models to predict the concentration in blood of $Y$ for $x=8$ $\mu$gr/dl.Is this prediction reliable. Justify your answer. 

Use the following sums:
$\sum x_i=52$ μg/dl, $\sum \log(x_i)=13.1955$ log(μg/dl), $\sum y_j=11.2$ μg/dl, $\sum \log(y_j)=3.253$ log(μg/dl), $\sum x_i^2=451.36$ (μg/dl)², $\sum \log(x_i)^2=26.9397$ log(μg/dl)², $\sum y_j^2=18.1$ (μg/dl)², $\sum \log(y_j)^2=1.5878$ log(μg/dl)², $\sum x_iy_j=86.57$ (μg/dl)², $\sum x_i\log(y_j)=26.3463$ μg/dl⋅log(μg/dl), $\sum \log(x_i)y_j=21.7087$ log(μg/dl)⋅μg/dl, $\sum \log(x_i)\log(y_j)=6.5224$ log(μg/dl)².

{{< spoiler text="Solution" >}}
1.

$\bar x=7.4286$ μg/dl, $s_x^2=9.2963$ (μg/dl)².<br/>
$\bar z=-0.7421$ μg/dl, $s_z^2=6.6664$ (μg/dl)².<br/>
$s_{xz}=-0.4147$ (μg/dl)²  
Linear relation: $r^2=0.9696$, that is close to 1, so there is a strong linear relation.  
2. Naming $u=\log(x)$ and $v=\log(y)$,  

$\bar u=1.8851$ log(μg/dl), $s_u^2=0.295$ log(μg/dl)².<br/>
$\bar v=0.4647$ log(μg/dl), $s_v^2=0.0109$ log(μg/dl)².<br/>
$s_{uv}=0.0558$ (μg/dl)²  
Potential relation: $r^2=0.9688$, that is close to 1, so there is a strong potential relation, although the linear relation is a little bit stronger.  
3. Regression line of $Y$ on $X$: $y=1.2153 + 0.0518x$.<br/>
$y(8)=1.6296$ μg/dl. The prediction is reliable since the linear coefficient of determination is close to 1.
{{< /spoiler >}}
