---
layout: post
title: "Feature Engineering: Using Weather Data to Predict Meal Consumption in a Military Mess"
date: 2020-04-06 17:50:00 +0900
author: "Shin Young Kim"
categories: bayesian feature-engineering
---

I was tasked to attempt to add weather data(precipitation, temperature) to enhance forecast results for meal consumption quantity in a military mess hall near Daejon, Korea.

The Data I recieved was daily meal consumption quantity from January 1st, 2019 to August 30th of the same year. Additionaly, some dates were missing from the data, which is believed to be from days which the mess didn't open, like holidays or leaves.

The plot below shows the consumption quantity plotted against dates, with selected peaks and floors marked as red and blue dots:

![data plot]({{site.url}}/images/blog/meal-date-plot.png)

Upon first look, some sort of seasonality can be seen, although not exact, since we have to remember that some dates are missing, meaning time axis is not uniform.

I tried plotting some autocorrelation plots of various lags to try to grasp seasonality intervals:

![data plot]({{site.url}}/images/blog/meal-date-acf-150.png)