---
layout: post
title: "Model Composition: Constructing a Hierarchical Spline Time Series Model"
date: 2020-04-06 17:24:06 +0900
author: "Jhin Woo Choi"
categories: bayesian model
---

A hierarchical spline time series model is being experimented on for forecasting failure rates.

The following properties were observed while configuring the model:

1. The sparsity of the data is unbalanced
2. Some portions of the data are missing
3. Each layer within the model shared similar properties


![]({{site.url}}/images/blog/sparsity_data.png)

*Sparsity data*


Data sparsity could be overcome by estimating B-Spline parameters, \\(\beta, w\\) for the overall period.

A hierarchical model can be constructed, and its hyperpriors estimated using Markov Chain Monte-Carlo sampling to handle missing data.

This method calculated the basis of B-Spline at equal intervals. It will be possible to build a more reliable model when calculating the basis by quantile division of the number of data according to the amount of data for each section.