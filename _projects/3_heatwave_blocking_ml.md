---
layout: page
title: Atmospheric blocking can trigger heatwaves but not always ! 
description: A small machine-learning study of atmospheric blocking and summer heatwaves (ERA5, 1979–2024)
img: assets/img/fig2_ml_models.png
importance: 1
category: data science
---

<div class="card p-3 mb-4 bg-light">
  <strong>The study in brief.</strong>
  Atmospheric blocking is weather patter which is persistent high pressure system that can trigger weather extremes.
   This is a small machine-learning part of a larger study on the link between blocking and heatwaves.
  <br><br>
  <a href="https://doi.org/10.5281/zenodo.23714803">Data and code (Zenodo)</a> ·
  <a href="https://github.com/Vinita-D/Blocking_to_heatwaves_ML">Machine-learning code (GitHub)</a>
</div>

**The question.** Can we predict a heatwave from the properties of a blocking: how long it lasts, how large
and strong it is, and where and when it occurs? And does a longer blocking bring severe heatwaves across mid latitudes?

**How.** Blocking and heatwaves are tracked as moving objects in ERA5 reanalysis (1979 to 2024): blocking from
an upper-atmosphere signal (potential vorticity), heatwaves from unusually hot surface temperatures. A blocking
is linked to a heatwave when their outlines overlap. About 800 blocking events, 13% of which were associated with
heatwave, This data is used to train a multivariate regression and a random forest (scikit-learn). They are tested on
summers they never saw, and compared with what chance alone gives, because a longer blocking has more days in
which a heatwave could occur simply due to longer overlapping timesteps

<div class="row justify-content-center">
  <div class="col-sm-12 mt-3">
    {% include figure.liquid path="assets/img/ml_2_training.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    <div class="caption">Whole summers are kept back for testing (a). The model learns from past blocking (b)
    and its predictions for unseen summers match what happened (c).</div>
  </div>
</div>

**Conclusions**
- Blocking is clearly linked to heatwaves: it meets them two to three times more often than chance.
- But a longer blocking does not clearly shows more frequent heatwaves or more severe heatwave events.
- Block size, persistence and position tell best whether a heatwave occurs, but not how intense, long or large it becomes. That needs more complex information, such surface fluxes, heat and moisture transport, soil moisture deficient etc.

<div class="row justify-content-center">
  <div class="col-sm-9 mt-3">
    {% include figure.liquid path="assets/img/ml_3_occurrence.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    <div class="caption">How often each kind of information picked the blocking that brought the heatwave
    (50% = guessing).</div>
  </div>
</div>

**Try the ML model : 27 June 2021.** The model found 3 blocking circulation in Norther hemisphere that day. It gave the highest
chance to the blocing over North America, the one that brought the record Pacific Northwest
heatwave.

| North American block | ML prediction | Real (ERA5) |
|---|---|---|
| Chance of a heatwave | 27% (highest of the 3) | heatwave occurred |
| Heatwave intensity | 11.0 K | 11.9 K |
| Heatwave duration | 5.8 days | 8.25 days |

**Tools:** Python, scikit-learn, xarray, pandas, ERA5.
Code: [github.com/Vinita-D/Blocking_to_heatwaves_ML](https://github.com/Vinita-D/Blocking_to_heatwaves_ML)
