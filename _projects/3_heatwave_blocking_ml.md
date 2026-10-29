---
layout: page
title: Which atmospheric blocks bring heatwaves?
description: A machine-learning diagnosis of ERA5 blocks and heatwaves with scikit-learn
importance: 1
category: data science
---

Blocking often triggers summer heatwaves, but which properties of a block matter? Starting from
about 800 Northern Hemisphere summer blocks (ERA5, June–August), I trained two machine-learning
models, logistic/linear regression and random forest (scikit-learn), to tell whether a block
brings a heatwave and what the heatwave is like. Each model is tested on summers it never saw.

More persistent blocks bring heatwaves more often: 8% of blocks lasting up to 6 days, 31% of
blocks lasting over 15 days. Block size, persistence and position tell heatwave occurrence best.
But block properties say little about how intense, long or large the heatwave becomes: that needs
more inputs, such as soil moisture and land-surface feedbacks.

Code: [github.com/Vinita-D/Blocking_to_heatwaves_ML](https://github.com/Vinita-D/Blocking_to_heatwaves_ML)
