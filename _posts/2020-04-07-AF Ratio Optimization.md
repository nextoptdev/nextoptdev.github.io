---
layout: post
title: "AF Ratio Optimization"
date: 2020-04-07 11:34:00 +0900
author: "Hyun Ji Moon"
categories: bayesian model-optimization
---

# AF Ratio Optimization

![AF ratio histogram]({{site.url}}/images/blog/af-ratio-plot.png)

*Histogram of AF ratios*

## Optimizing the distribution of A/F ratio for the maximum profit by using historical data. Inform about the best decision for order quantity.
 Solution for how to optimize this A/F data, which is right-skewed and limited to positive values. Yield different models depending on an allowing range and the amount of data.

### Challenge
  How to fit the A/F ratio distribution under partial demand and forecast information

### Solution
 Through Entropy Maximization, find optimal inventory levels with uncertain demand distribution.

### Why?
  Balance between risk and benefit of ordering is important. Focusing on the proportion casts light on optimal order quantity and has an advantage of normalizing, rather than exact prediction of actual quantity.

### How?
 Estimate the optimal distribution by calculating and comparing the resulting profits between various competing distributions.