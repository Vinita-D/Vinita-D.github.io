---
layout: page
title: Tracking heatwaves in space and time (Quasi-Lagrangian heatwaves)
description: Open-source code that follows heatwaves and blocks through space and time
img: assets/img/gallery_output.png
importance: 2
category: research software
---

How do you find a heatwave in data? The usual way is to pick a place and check when its daily maximum temperature stays above normal for several days. But heatwaves are not fixed to one place: they are large patches of hot air that move, grow and change shape ([Luo et al., 2022](https://doi.org/10.1029/2022GL097714)). It is a useful tool I build , to detect and track weather patterns and here I am showing an example of detected record breaking heatwave (orange color in the figure below)and its associated atmopsheric blocking (in white)

This code follows each heatwave as **one moving object**, from its start to its end. It uses two different approches of tracking avaiable at: [github.com/Vinita-D/Quasi_Lagrangian_heatwave_detection](https://github.com/Vinita-D/Quasi_Lagrangian_heatwave_detection)
<div class="row justify-content-center">
  <div class="col-sm-10 mt-3">
    {% include figure.liquid path="assets/img/gallery_output.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    <div class="caption">The record-breaking 2021 heatwave in North America: the detected heatwave (orange) and the block, shown as a circle (white).</div>
  </div>
</div>


