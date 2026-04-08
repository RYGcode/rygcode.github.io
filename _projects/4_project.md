---
layout: page
title: AMC in wireless communication using CNN 
description: my academic project
img: assets/img/img_2.jpg
importance: 1 
category: academic
---


Modern communication systems are not static. They constantly deal with changing environments, noise, and unpredictable signals. Because of that, systems need to be adaptive. This is where my project started. I wanted to explore how we can automatically recognize different types of signal modulation in a smarter way.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/img_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/img_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

I focused on Automatic Modulation Recognition or AMR, which allows a system to understand what kind of signal it is receiving. Instead of manually analyzing signals, I used machine learning so the system can learn patterns by itself.

One of the main challenges was handling complex signal data. Raw data is not always easy for a model to understand, so I transformed it into more meaningful forms like constellation diagrams and 2D CSV representations. With this approach, the model can capture the unique characteristics of each modulation type. In this project, I worked with six different types of modulation.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/img_7.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/img_8.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

For the model, I used Convolutional Neural Networks or CNN. Even though CNN is often used for image processing, it works well here because the transformed signal looks like patterns that can be learned visually. The data was generated from signals received using Software Defined Radio and simulated with Simulink. I also used four different synchronization types because signal conditions can vary depending on how they are received.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/img_9.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/img_10.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

After going through training, validation, and testing, the results were quite satisfying. The model achieved 95.4 percent accuracy on validation data and 96.5 percent on test data. It also only takes around 0.00008 seconds to recognize one type of modulation, which shows that the model is not only accurate but also fast.

