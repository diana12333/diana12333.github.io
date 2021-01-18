---
title: "Sydney Weather Forecasting"
excerpt: "A weather forcasting model based on the multivariate time series analysis model VAR, disucssion and comparing to ARIMA and LSTM"
header:
  image: /assets/images/unsplash-gallery-image-2.jpg
  teaser: assets/images/unsplash-gallery-image-2.jpg
  caption: "Photo credit: [Google](https://www.cushmanwakefield.com/en/australia/offices/sydney)"
sidebar:
  - title: "Role"
    image: http://placehold.it/350x250
    image_alt: "logo"
    text: "Designer, Front-End Developer"
  - title: "Responsibilities"
    text: "Reuters try PR stupid commenters should isn't a business model"
gallery:
  - url: /assets/images/unsplash-gallery-image-1.jpg
    image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
  - url: /assets/images/unsplash-gallery-image-2.jpg
    image_path: assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
  - url: /assets/images/unsplash-gallery-image-3.jpg
    image_path: assets/images/unsplash-gallery-image-3-th.jpg
    alt: "placeholder image 3"
---

Background 
===========

Weather forecasting is the application of science and technology to predict the conditions of the atmosphere for a given location and time, it relates closely to Production activities, social activities and daily activities. Forecasting weather requires interdisciplinary knowledge. Traditionally, the weather forecasting models were made by collecting as much data as possible about the current state of the atmosphere (temperature, humidity, rainfall meteorology understanding and wind), this processing can be complicated and only valid to short term forecasting. 


In this project, we applied time series analysis models to resolve the long term weather forecasting challenge. More details about the VAR/VARMA/LSTM models and the model evaluation and discussion are included in the report [here](/assets/doc/weather-forcast/VAR_MultivariateTimeSeriesAnalysis.pdf). 


Exploratory Data Analysis 
===========
The original data include 72588 observations of 46 different weather stations recordings, which was extracted from the bureau of the Australia meteorology with date from 2013-03-01 to 2017-06-25. Missing data is imputed with linear Interpolation Imputation.


A shiny App was built [here](https://changshen.shinyapps.io/shiny/).

<img src="/assets/gif/demo2.gif" width="400" height="400" />

{% include gallery caption="detail" %}

