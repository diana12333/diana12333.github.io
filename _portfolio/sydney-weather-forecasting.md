---
title: "Sydney Weather Forecasting"
excerpt: "A weather forecasting model based on the multivariate time series analysis model VAR, discussion and comparing to ARIMA and LSTM"
header:
  image: /assets/images/unsplash-gallery-image-2.jpg
  teaser: assets/images/unsplash-gallery-image-2.jpg
  caption: "Photo credit: [Google](https://www.cushmanwakefield.com/en/australia/offices/sydney)"
# sidebar:
#   - title: "Role"
#     image: http://placehold.it/350x250
#     image_alt: "logo"
#     text: "Designer, Front-End Developer"
#   - title: "Responsibilities"
#     text: "Reuters try PR stupid commenters should isn't a business model"
gallery:
  - image_path: assets/images/weather-forecasting/seasonality.png
    alt: "placeholder image 1"
    excerpt: "In the Exploratory Data Analysis part, I applied several visualizations and analysis to better understand the raw data."
    url: "https://github.com/diana12333/R-project/tree/master/Multivariate%20Time%20Series"
    btn_label: "Read More"
    btn_class: "btn--primary"
gallery2:
  # - url: /assets/images/weather-forecasting/Stationary.png
  #   image_path: assets/images/weather-forecasting/Stationary.png
  #   alt: "placeholder image 2"
  - image_path: assets/images/weather-forecasting/result.jpg
    alt: "placeholder image 3"
    excerpt: "LSTM model forecasting and the VAR(order 1/order 2) are demostrated as right, blue curve is the true value. VAR(1) has the best perfomance considering the model complexity and accuracy."
    url: "https://github.com/diana12333/R-project/tree/master/Multivariate%20Time%20Series"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

Background 
===========

Weather forecasting is the application of science and technology to predict the conditions of the atmosphere for a given location and time, it relates closely to Production activities, social activities and daily activities. Forecasting weather requires interdisciplinary knowledge. Traditionally, the weather forecasting models were made by collecting as much data as possible about the current state of the atmosphere (temperature, humidity, rainfall meteorology understanding and wind), this processing can be complicated and only valid to short term forecasting. 


In this project, we applied time series analysis models to resolve the long term weather forecasting challenge. More details about the VAR/VARMA/LSTM models and the model evaluation and discussion are included in the report. 


Exploratory Data Analysis 
===========
The original data include 72588 observations of 46 different weather stations recordings, which was extracted from the bureau of the Australia meteorology with date from 2013-03-01 to 2017-06-25. Missing data is imputed with linear Interpolation Imputation.


A shiny App was developed [here](https://changshen.shinyapps.io/shiny/).

<img src="/assets/gif/demo-weather-forcasting.gif" width="800" height="800" />

Methods and Discussions 
==========
* **VAR(Vector Autoregression)**


   A linear model designed for multivariate time series. It’s a generalization of the AR(Autoregression) model by including the capture of the linear interdependencies among multiple time series. A baseline model and a VAR with the seasonal dummy terms are modeled in this study where the order of time series models is determined with AIC/HQ/SC/FPE. 
* **Model Diagnose**


  Model assumption(Correlation/Heteroscedasticity/Normality) were validated.
 
* **LSTM(Long Short Term Memory Neural Network)**


  Long Short Term Memory (LSTM) networks are a special Recurrent Neural Network (RNN) that are capable of learning long-term dependencies. Here it was applied for leveraging the multivariate time series modeling problem.


{% include feature_row id="gallery" type="left" %}
{% include feature_row id="gallery2" type="right" %}
Presentation
==========
<iframe src="https://slides.com/changshen/multivariate/embed" width="576" height="420" scrolling="no" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>



[See report here](/assets/doc/weather-forcast/VAR_MultivariateTimeSeriesAnalysis.pdf){: .btn .btn--primary}