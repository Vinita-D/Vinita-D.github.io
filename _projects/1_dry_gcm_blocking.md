---
layout: page
title: Can a dry model reproduce atmospheric blocking?
description: Atmospheric blocking in a dry general circulation model
img: assets/img/gcm_dry.png
importance: 4
category: research
---

Idealised simulations are a classic way to understand how the atmosphere works. I used a dry
general circulation model from IPSL (DYNAMICO): an atmosphere with no ocean and no water. To bring
it as close as possible to the real world, we adjusted its forcing step by step, with an iterative
method, until its climate matched the observed one.

The idea: by removing water, we can see what water/moisture does. Comparing the dry model with the real
atmosphere (ERA5) shows the role of moisture, ironically through its absence.
The result: the dry model reproduces blocking remarkably well. But the air that builds the blocks
travels differently. Tracing it backwards in time (Lagrangian trajectories) shows that in the real
atmosphere, part of this air rises and is heated by condensation, which a dry model cannot do.

{% include figure.liquid path="assets/img/projects/dry_gcm.png" class="img-fluid rounded z-depth-1" zoomable=true %}
<div class="caption">[schematic representing the main air masses entering the blocking ridge at the blocking onset for (a) reanalysis and (b) dry model. ]</div>

Paper: [Journal of the Atmospheric Sciences, 2024](https://doi.org/10.1175/JAS-D-24-0048.1)
