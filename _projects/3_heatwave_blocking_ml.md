---
layout: page
title: Which atmospheric blocing triggers heatwave? (not all of them!)
description: A machine-learning diagnosis of ERA5 blocking and heatwaves with scikit-learn
img: assets/img/fig2_ml_models.png
importance: 1
category: data science
---

<div class="card p-3 mb-4 bg-light">
  <strong>The study in brief.</strong>
  This is a part of the study to investigate non-local link between blocking and heatwaves; key findings of this project-
  Blocking is clearly linked to heatwaves: Persistence of blocking brings heatwaves more often, and heatwaves under blocking are hotter. But block
  strength does not set how severe a heatwave becomes. Heatwaves and atmospheric blocks were detected and tracked as moving objects in ERA5 (1979–2025).
  Blocks are linked to heatwaves when their circles overlap. 
  <br><br>
  <a href="https://doi.org/10.5281/zenodo.23714803">Data and code (Zenodo)</a> ·
  <a href="https://github.com/Vinita-D/Blocking_to_heatwaves_ML">ML code (GitHub)</a>
</div>

Blocking often triggers summer heatwaves, but which properties of blocking matter? From about 43 summer blocks (ERA5, June–August), I trained two machine-learning models (regression and random forest, scikit-learn) to tell whether a block brings a heatwave, and what that heatwave is like. Each model is tested on summers it never saw.

**What I found:** longer-lasting blocks bring heatwaves more often (8% of blocks up to 6 days, 31% of blocks over 15 days). Block size, persistence and position tell best whether a heatwave occurs, but not how intense, long or large it becomes. That needs more complex information, such as soil moisture.

<div class="row justify-content-center">
  <div class="col-sm-10 mt-3">
    {% include figure.liquid path="assets/img/fig2_ml_models.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

**Try it on a real day: 27 June 2021.** The model found 3 blocks that day. It gave the highest
chance to the block over North America, the one that brought the record Pacific Northwest
heatwave.

| North American block | ML prediction | Real (ERA5) |
|---|---|---|
| Chance of a heatwave | 27% (highest of the 3) | heatwave occurred |
| Heatwave intensity | 11.0 K | 11.9 K |
| Heatwave duration | 5.8 days | 8.25 days |

<div class="row justify-content-center">
  <div class="col-sm-10 mt-3">
    {% include figure.liquid path="assets/img/blocks_2021-06-27.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    <div class="caption">The blocks on 27 June 2021, coloured by their chance of bringing a heatwave. The star marks the heatwave.</div>
  </div>
</div>

Code: [github.com/Vinita-D/Blocking_to_heatwaves_ML](https://github.com/Vinita-D/Blocking_to_heatwaves_ML)
