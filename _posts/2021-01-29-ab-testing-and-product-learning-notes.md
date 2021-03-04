---
title: "AB testing and Product Learning Notes"
date: 2021-12-31
categories:
  - Notes
tags:
  - data science
  - product
  - interview
toc: true
toc_sticky: true
---

## Introduction and Motivation
### **Online controlled experiment(A/B testing)**
#### The most common online experiment setting
  - Users are randomly split between variants in a persistent manner. It has two groups in the simplest version: Treatment B and Control A.


- **Overall Evaluation Criterion**(OEC) quantitive measure of the experiment's objective, e.g. DAU, LTV, session per user(usage), relevance(time to success). 
  The requirement for OEC:
  
  1.  Measurable in the short term 
  2.  Causally drive long-term strategic objective

Metric teams: choosing metrics, validating metrics and evolving metric over time 

### Motivation
#### Case desciption: 
  - Increase the user churn rate in a subscription business, e.g. Amazon Prime, Spotify memebership. To achieve this we may need to introduce a new feature and prove there is **causal relationship** between the new feature and the user churn rate. 
  causal inference related knowledge might required in this process. A thing we need to remember is **Correlation doesn't imply causality**.
  <figure>
	<a href="/assets/images/abtesting/hirarachypyramid.png"><img src="/assets/images/abtesting/hirarachypyramid.png"></a>
	<figcaption><a href="https://www.cambridge.org/core/books/trustworthy-online-controlled-experiments/introductory-topics-for-everyone/9C9CAEDA5A192FF74D5EBACEB44886F0" title="">hierarchy of evidence of assessing the quality of trial design</a>.</figcaption>
</figure>

#### Motivation:
 * Establish causality with high probability
 * Detect minor and unexpected changes 



## Running and Analyzing the experiment 

#### <u> Case study </u>

* **Objective** marketing departments want to increase sales by sending coupon codes/ promotion code for discount.  by simply adding a coupon field at the check out page. We need to evaluate the effect of changing UI. Access the feasibility of the new business model.

* **Concerns** The newly added field would distract people from checking out, further leads to revenue decreasing.

* **Approaches** Fake door/ painted door approaches.

* **Goal Metrics** Revenue per user; randomization unit is user

* **Users included** The users who start the purchasing process
  * **Not all users**: noisy since most of the users won't even start the process
  * **Not the users who complete purchase**:

* **Hypothesis Testing**
1. baseline mean(for most metrics) and standard error
2. experiment size/randomized units/how long to run
3. statistical significance and practical significance 

* **How long to run the experiment**
1. **More users** need to be included -- to increase the statistical power.
2. **Day-of-week effect** -- capture the weekly cycle-- experiment longer than 1 week
3. **Seasonality** -- e.g holidays
4. **Primacy and novelty effects** experiments take time to stablize 

> Before interpret the result, we might need to have a sanity check 


#### Results to decisions

* **Case one**: no statistical significance and practical significance and the CI is not very wide or small. **Reiterate/abandon the idea**.
* **Case two**: both statistically significant and practical significance. **Launch**
* **Case three**: have statistical significance but not practical significance **Discuss whether it worths it**.
* **Case four**: Confidence Interval is very wide, **Include more units** gain more power.

* **Case 5**: practical significant and not statistical significant **repeat the experiment**

## Experiment Trustworthiness 

#### **Extreme results**
* **potential explanations**
  - instrumentation(logging)
  - computational error
  - loss of data

#### **Misinterpretation of the result**
* **Common errors**
  - Lack of power
  - P-values interpretation: the level of marginal significance within a statistical hypothesis test representing the probability of the occurrence of a given event.

#### **Multiple Comparisons**
* **Common senarios** 
  - Multiple metrics
  - P-values over time
  - Population segementation
  - multiple iterations


#### **Confidential Interval**
quantify the degree of uncertainty in the treatment effect

Interpretation of CI: how often the CI computed from many studies would contain the true treatment effect.

#### **Internal Validity**
* **SUTVA** -- no interection 
  - **exmaple of violations**: social networks;communication tools; collaboration tools; shared documentation; two-sided market(ebay/uber/lyft)

* **Intention to Treat**
* **Survivorship Bias**
* **Sample Ratio Mismatch(SRM)**
  * Browser redirect
  * Lossy instrumentation 
  * Residual or carryover effect

#### **External Validity(Generalization)**
#### **Primary Effect and Novelty effect**
* highlight by take the new users

#### **Segementation**
* Market/Country
* Device/Platform
* Time of Day/Day of Week
* User Type(new/existing/returning)
* Single/Shared/Family
> Conditional Average Treatment Effect in causal inference

#### **Simpson Paradox**
<img src="https://latex.codecogs.com/svg.latex\small?&space;\frac{b}{a}<\frac{B}{A},\frac{d}{c}<\frac{D}{C},\frac{b+d}{a+c}>\frac{B+D}{A+C}"/> 

* Possible reasons:
  * Different Treatment/Control Assignment in different segementation.
  * Sampled not uniform








### Task Lists


- [x] Introduction and the Motivation
- [x] Runing and Analyzing Experiment: An end to end example 
- [x] Experiment trustworthiness

> Based on the book **Trustworthy Online controlled experiments**