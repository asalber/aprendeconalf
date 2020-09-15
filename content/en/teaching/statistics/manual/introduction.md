---
title: Introduction
summary: " " 
date: 
lastmod:
tags: [Statistics]
categories: [Statistics, Biostatistics]
type: book
weight: 5
---

## Statistics as a scientific tool

### What is Statistics?

{{% alert def %}}
**Definition - Statistics**. _Statistics_ is a branch of Mathematics that deals with data collection, summary, analysis and interpretation.
{{% /alert %}}

The role of Statistics is to extract information from data in order to gain knowledge for taking decisions.

![Statistics purpose.](../img/introduction/statistics_purpose.png "Statistics purpose")

Statistics is essential in any scientific or technical discipline which requires data handling, especially with large volumes of data, such as Physics, Chemistry, Medicine, Psychology, Economics or Social Sciences.

But, _why is Statistics necessary?_

### A changing World

Scientists try to study the World. A World with a high variability that makes difficult determining the behaviour of things.

Statistics provides a bridge between the real world and the mathematical models that attempt to explain it, providing a methodology to assess the discrepancies between reality and theoretical models.

This makes Statistics an indispensable tool in applied sciences that require design of experiments and data analysis.

## Population and sample

### Statistical population

{{% alert def %}}
**Definition - Population**. A _population_ is a set of elements defined by an or more features that has all the elements and only them. Every element of the population is called _individual_.

**Definition - Population size**. The number of individuals in a population is known as the _population size_ and is represented by $N$.
{{% /alert %}}

Sometimes not all the individuals are accessible to study. Then we distinguish between:

- **Theoretical population**: Individuals to which we want to extrapolate the study conclusions.
- **Studied population**: Individuals truly accessible in the study.

**Example**. In a study about a particular disease, the theoretical population would be all the persons that suffered the disease in some moment, even if they were not born yet. While the studied population will be the set o persons that have suffered the disease and that we can really study (observe that this exclude people with the disease but that we do not have any mean to get information about them).

### Drawbacks in the population study

Scientists study a phenomenon in a population to understand it, to get knowledge about it, and so to control it.

But, for a complete knowledge of the population it is necessary to study all its individuals.

However, this is not always possible for several reasons:

- The population size is infinite or too large to study all its individuals.
- The operations that individuals undergo are destructive.
- The cost, both in money and time, that would require study all the individuals in the population is not affordable.

### Statistics Sample

When it is not possible or convenient to study all the individuals in a population, we study only a subset of them.
{{% alert def %}}
**Definition - Sample**. A _sample_ is a subset of the population.

**Definition - Sample size**. The number of individuals of the sample is called _sample size_ and is represented by $n$.
{{% /alert %}}

Usually, the population study is conducted on samples drawn from it.

The sample study only gives an approximate knowledge of the population. But in most cases it is _enough_.

### Sample size determination

One of the most interesting questions that arise:

_How many individuals are required to sample to have an approximate but enough knowledge of the population?_

The answer depends of several factors, as the population variability or the desired reliability for extrapolations to the population.

Unfortunately we can not answer that question until the end of the course, but in general, the most individuals the sample has, the more reliable will the conclusions be on the population, but also the study will be longer and more expensive.

**Example**. To understand what a sufficient sample size means we can use a picture example. A digital photography consist of a lot of small points called pixels disposed in an big array layout with rows and columns (the more rows and columns, the more resolution the picture has). Here the picture is the population and every pixel is an individual. Every pixel has a colour and it is the variability of colours what forms the picture motif.

_How many pixels must we take in a sample in order to know the motif of a picture?_

The answer depends on the variability of colours in the picture. If all the pixels in the picture are of the same colour, only one pixel is required to know the motif. But, if there is a lot of variability in the colours, a large sample size will be required.

The image below contains a small sample of the pixels of a picture. Could you find out the motif of the picture?

![Picture with low resolution.](../img/introduction/sample_windmill1.jpg "Picture with low resolution.")

_With a small sample size it is difficult to find out the picture motif!_

Surely you has not been able to guess the motif because the number of pixels picked in the sample is too small to understand the variability of colours in the picture.

The image below contains a larger sample of pixels. Could you find out the motif of the picture now?

![Picture with medium resolution.](../img/introduction/sample_windmill2.jpg "Picture with medium resolution.")

_With a large sample is easier to find out the picture motif!_

And here is the whole population.

![Picture with full resolution.](../img/introduction/sample_windmill3.jpg "Picture with full resolution.")

_It is not required to know all the pixels of a picture to find out its motif!_

### Types of reasoning

<img src="../img/introduction/types_reasoning.png" alt="Types of reasoning" width="400px">

**Deduction properties**: If the premises are true, it guarantees the certainty of the conclusions (that is, if something is true in the population, it is also true in the sample). However,

**Induction properties**: It does not guarantee the certainty of the conclusions (if something is true in the sample, it may not be true in the population, so be careful with the extrapolations!). But, _it is the only way to generate new knowledge!_

Statistics is fundamentally based on inductive reasoning, because it uses the information obtained from samples to draw conclusions about populations.

## Sampling
{{% alert def %}}
**Definition - Sampling**. The process of selecting the elements included in a sample is known as _sampling_.
{{% /alert %}}

![Sampling](../img/introduction/sampling.png)

To reflect reliable information about the whole population, the sample must be representative of the population. That means that the sample should reproduce on a smaller scale the population variability.

_The goal is to get a representative sample of the population._

### Types of sampling

There exist a lot of sampling methods but all of them can be grouped in two categories:

**Random sampling**: The sample individuals are selected randomly. All the population individuals have the same likelihood of being selected (_equiprobability_).

**Non random sampling**: The sample individuals are not selected randomly. Some population individuals have a higher likelihood of being selected than others.

Only random sampling methods avoid the selection bias and guarantee the representativeness of the sample, and therefore, the validity of conclusions.

Non random sampling methods are not suitable to make generalizations because they do not guarantee the representativeness of the sample. Nevertheless, usually they are less expensive and can be used in exploratory studies.

### Simple random sampling

The most popular random sampling method is the _simple random sampling_, that has the following properties:

- All the population individuals have the same likelihood of being selected in the sample.
- The individual selection is performed with replacement, that is, each selected individual is returned to the population before selecting the next one. In this way the population does not change.
- Each individual selection is independent of the others.

The only way of doing a random sampling is to assign a unique identity number to each population individual (conducting a _census_) and performing a random drawing.

## Statistical variables

In every statistical study we are interested in some properties or characteristics of individuals.

{{% alert def %}}
**Definition - Statistical variable**. A _statistical variable_ is a property or characteristic measured in the population individuals.
{{% /alert %}}

The _data_ is the actual values or outcomes recorded on a statistical variable.

![Statistical variables](../img/introduction/statistical_variables.png)

### Types of statistical variables

According to the nature of their values and their scale, they can be:

- **Qualitative variables**. They measure non-numeric qualities. They can be:

  - **Nominals**: There is no natural order between its categories. Example: The hair colour or the gender.

  - **Ordinals**: There is a natural order between its categories. Example: The education level.

- **Quantitative variables**: They measure numeric quantities. They can be:

  - **Discrete**: Their values are isolated numbers (usually integers). Example: The number of children or cars in a family.

  - **Continuous**: They can take any value in a real interval. Example: The height, weight or age of a person.

Qualitative and discrete variables are also called _categorical variables_ and their values _categories_.

<img src="../img/introduction/variable_types.svg" alt="Types of statistical variables" width="800px">

#### Choosing the appropriate type of variable

Sometimes a characteristic could be measured in variables of different types.

**Example**. Whether a person smokes or not could be measure in several ways:

- Smokes: yes/no. (Nominal)

- Smoking level: No smoking/unusual/moderate/quite/heavy. (Ordinal)

- Number of cigarettes per day: 0,1,2,...(Discrete)

In those cases quantitative variables are preferable to qualitative, continuous variables are preferable to discrete variables and ordinal variables are preferable to nominal, as they give more information.

<img src="../img/introduction/variable_information.svg" alt="Amount of information of the different types of variables" width="600px">

According to their role in the study:

- **Independent variables**: Variables that do not depend on other variables in the study. Usually they are manipulate in an experiment in order to observe their effect on a dependent variable. They are also known as _predictor variables_.

- **Dependent variables**: Variables that depend on other variables in the study. They are not manipulated in an experiment and are also known as _outcome variables_.

**Example**. In a study on the performance of students in a course, the intelligence of students and the daily study time are independent variables, while the course grade is a dependent variable.

### Types of statistical studies

According to their role in the study:

- **Experimental**: When the independent variables are manipulated in order to see the effect that that change has on the dependent variables.  
  **Example**. In a study on the performance of students in a test, the teacher manipulates the methodology and creates two or more groups following different methodologies.

- **Non-experimental**: When the independent variables are not manipulated. That does not mean that it is impossible to do so, but it will either be impractical or unethical to do so.  
  **Example**. In a study a researcher could be interested in the effect of smoking over the lung cancer. However, whilst possible, it would be unethical to ask individuals to smoke in order to study what effect this had on their lungs. In this case, the researcher could study two groups of people, one with lung cancer and other without, an observe in each group how many persons smoke or not.

Experimental studies allow to identify a cause and effect between variables while non-experimental studies only allow to identify association or relationship between variables.

### The data table

The variables of a study will be measured in each individual of the sample. This will give a data set that usually is arranged in a tabular form known as _data table_.

In this table each column contains the information of a variable and each row contains the information of an individual.

**Example**. The table below contains data about the variables Name, Age, Gender, Weight and Height of a sample of 6 persons.

| Name               | Age | Gender | Weight(Kg) | Height(cm) |
|:-------------------|:---:|:------:|:----------:|:----------:|
| José Luis Martínez | 18  |   H    |     85     |    179     |
| Rosa Díaz          | 32  |   M    |     65     |    173     |
| Javier García      | 24  |   H    |     71     |    181     |
| Carmen López       | 35  |   M    |     65     |    170     |
| Marisa López       | 46  |   M    |     51     |    158     |
| Antonio Ruiz       | 68  |   H    |     66     |    174     |

## Phases of a statistical study

Usually a statistical study goes through the following phases:

1. The study begins with a previous design in which the study goals, the population, the variables to measure and the required sample size are set.

2. Next, the sample is selected from the population and the variables are measured in the individuals of the sample (getting the data table). This is accomplished by _Sampling_.

3. The next step consists in describing and summarizing the information of the sample. This is the job of _Descriptive Statistics_.

4. Then, the information obtained is projected on a mathematical model that intend to explain what happens in population, and the model is validated. This is accomplished by _Inferential Statistics_.

5. Finally, the validated model is used to perform predictions and to draw conclusions on the population.

### The statistical cycle

<img src="../img/introduction/statistical_cycle.svg" alt="Statistical cycle" width="600px">
