---
layout: page
title: MobiTang
description: Mobil widget interaction using signal processign and machine learning.
img: assets/img/mag.png
importance: 2
category: work
---

The proliferation of touch screen technology in various consumer electronic devices such as smartwatches, smartphones, and smart TV controls has presented a number of challenges related to the utilization of flat touchscreens. Most notable of these challenges is the ”fat finger problem” which obstructs content on the screen. Additionally, there is a lack of controls in certain applications, such as video games, necessitating an innovative solution. To address these issues, this proposed research endeavors to prove validity of physical widgets that can be attached to smartphones, providing supplementary control options through various interactions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/framework_left.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/framework_front.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/framework_right.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Lateral and Front View of Proposed Framework
</div>

The framework has three distinct widgets, `button`, `slider` and `rotary`. Each widget has a metal alloy corresponding to it that moves as the user interacts with the widget. The disruption in magnetic field around the framework as user interacts with the widgets is captured using the magnetometer inside the smartphone.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/button_phyphox.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/slider_phyphox.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/rotary_phyphox.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Magnetometer Readings For Widget Interactions
</div>
The signals recorded using the magnetomter are processed before being passed into the machine learning pipeline for widget prediction.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pipeline.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This is the signal processing pipeline.
</div>

After testing various models using pycaret, following were the results for the best model, which was the Extra Trees classifer.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/confmat_cv_5.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Confusion matrix using 5-fold cross validation for all interactions included when no interaction was made (raw).
</div>

