---
title: "Helper Function in R"
layout: single
author_profile: false
share: true
excerpt: "Some R helper fuctions I wrote. Update: Emperical.power;plot.emperical.power;StrarifiedRandomize"
header:
  image: /assets/images/random.jpg
  teaser: /assets/images/random.jpg
sidebar:
  - title: "Chang Shen"
    image: /assets/images/bio-photo.jpg
    image_alt: "logo"
    text: "Self-motivated, dedicated to data science in healthcare industry."
tags: 
  - Simulation
  - R developing
gallery:
  - url: /assets/images/gallery/EmpricalPower1.png
    image_path: assets/images/gallery/EmpricalPower1.png
    alt: "placeholder image 1"
  - url: /assets/images/gallery/EmpricalPower2.png
    image_path: assets/images/gallery/EmpricalPower2.png
    alt: "placeholder image 2"
  - url: /assets/images/gallery/NN.jpg
    image_path: assets/images/gallery/NN.jpg
    alt: "placeholder image 3"
---

Introduction
=======
MyRFunction is a package that was built and maintained by Chang Shen. Implemented serveral reproducible functions including statistical simulation, statistical learning and visualization. Free feel to fork it from my github page and reuse it

Functions
========

* **Stratified**: Simulation of a stratified randomization for a two-arm study.

* **Emperical.power**: Generate a dataframe with each sample size(N), alpha(level of significance), sd(the standard deviation of groups), delta(he true different between group2 and group1),  true mean of group1 and the true power and emperical power with simulation

* **plot.emperical.power**: Visualize the result of **Emperical.power** function

* **knnclass**: An naive implemention of K nearest neighboors algorithm

* **train_nn**: An simple neural network modelling function and result visualiztion

{% include gallery caption="This is a sample gallery to go along with this case study." %}
