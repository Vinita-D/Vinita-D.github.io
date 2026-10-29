---
layout: page
title: Can a dry model reproduce atmospheric blocking?
description: What blocking looks like in an atmosphere without water
img: assets/img/gcm_dry.png
importance: 4
category: research
---

To understand how the atmosphere works, scientists often simplify it by using idealised modelling. I used a dry general
circulation model from IPSL (DYNAMICO): an atmosphere with no ocean and no water. We tuned its forcing step by step until its climate matched the real one.

**The idea:** remove the water, and you see what water does. Comparing the dry model with the real atmosphere (ERA5) reveals the role of moisture, ironically through its absence.

**The result:** the dry model reproduces blocking remarkably well. But the air that builds the
blocks travels differently. Tracing it backwards in time shows that in the real atmosphere, part
of this air rises and is heated by condensation, which a dry model cannot do.

<div class="row justify-content-center">
  <div class="col-sm-10 mt-3">
    {% include figure.liquid path="assets/img/gcm_dry.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    <div class="caption">The main air masses entering the blocking ridge at blocking onset, red color are the moisture inflused airmass and blue are the dry airmass(a) in the real atmosphere (ERA5) and (b) in the dry model.</div>
  </div>
</div>

Paper: [Journal of the Atmospheric Sciences, 2024](https://doi.org/10.1175/JAS-D-24-0048.1)
