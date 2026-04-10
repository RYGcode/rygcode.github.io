---
layout: page
title: Eden App
description: bangkit academy project
img: assets/img/img_5.png
importance: 2
category: academic
---

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/img_13.jpg" title="Eden App" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Building Eden: From Idea to Reality

I started this project from something that actually feels very real today climate change. It is not just a theory anymore, we can see the impact slowly happening. The temperature of the earth keeps increasing, and one of the scary effects is rising sea levels. In the future, many cities might be affected, even Jakarta.
One of the main reasons behind this problem is carbon emissions that are still hard to reduce. Forests actually help a lot by absorbing carbon, but sadly deforestation is still happening. Because of that, the natural filter of our earth is slowly decreasing.
From this situation, I realized that solving climate change is not only about big actions. Small actions from people also matter. With the large number of Android users in Indonesia, my team and I thought maybe we can use technology to invite people to start from something simple, like gardening at home.
That is how the idea of Eden came. We wanted to introduce planting culture to younger generations using a more modern way, with the help of machine learning. The goal is simple, helping people build a habit of gardening while also increasing awareness about protecting the environment. We also added a gamification concept so it feels more engaging, not just another boring app.


### How We Developed the App

During this project, we followed three main paths from Bangkit program: machine learning, mobile development, and cloud computing.
For machine learning, we focused on building an image classification model. On the mobile side, the app was developed using Kotlin. And for cloud computing, we handled the integration between the model and the app, including data storage.
At first, we tried using a Convolutional Neural Network (CNN) model. But the results were not that good. The accuracy was still quite low. Then we tried another approach using transfer learning, and surprisingly it gave much better results. The model reached around 90% accuracy with about 88% validation accuracy.
That was a big improvement compared to the first attempt.


### Building the Machine Learning Model

The process started with collecting data. We gathered images from the internet using web scraping because it was quite difficult to find a free and complete dataset. Doing it manually would take too much time, so automation really helped here.
At the beginning, we collected around 50 types of ornamental plants, each with around 500 to 1000 images. But not all of them were usable. So we filtered and selected only the valid ones, and finally we decided to use 16 classes for training.
After collecting the data, the next step was preprocessing. The images had different formats and sizes, so we needed to standardize them. We split the dataset into training and testing folders, resized all images to the same size, and normalized them so the model can process them properly.
We also applied data augmentation like rotation, zoom, shift, and flipping. This helps increase the variation of the dataset, so the model can learn better.


### Training the Model

At first, we built a CNN model with several layers like Conv2D, max pooling, flatten, and dropout. The idea was to extract features from images and then classify them.
But after training, the result was not satisfying. The model only reached around 70% accuracy and even lower validation accuracy. This means the model still made many mistakes when predicting new images.
To improve this, we reduced the number of classes and tried another approach using transfer learning. We used MobileNetV2 as the pretrained model.
This approach worked much better. After training, the model reached around 90% accuracy with 88% validation accuracy. It was a huge improvement, andthe predictions on new images were also quite accurate.
At that point, we felt confident enough to move to the next step.


### Deployment

After training, we prepared the model for deployment. There are two approaches we used.
The first one is converting the model into TensorFlow Lite format. This allows the model to run directly on mobile devices, which is faster and simpler for integration.
The second approach is using Flask and Docker to build an API. The model is loaded into a backend server, and the app can send requests to this API to get predictions. We tested this using Postman before deploying it to the server.
Both methods were prepared to make it easier for both mobile and cloud teams to continue development.


### Testing the Model

We tested the model using several real images. And honestly, the results were quite satisfying.
For example, when testing a sunflower image, the model correctly predicted it. The same goes for other plants like spider plant (Chlorophytum Comosum) and Snow White Aglaonema.
Even with images that the model had never seen before, it was still able to give correct predictions most of the time.


### Final Result: The Eden App

In the end, we built Eden with several main features.
There is a login system so users can create and access their account. Then there is a plant donation feature, where users can share plants with others while earning points.
We also added a plant list feature to help users keep track of their plants, including reminders and recommendations.
And the main feature is plant classification. Users can take a photo of a plant, and the app will identify it using the trained model. It also provides additional information like how to take care of the plant.


### Closing Thoughts

This project gave me a lot of new experience, especially in machine learning. I learned not only about building models, but also how to apply them to solve real problems.
I also realized that having more and cleaner data really affects the model performance. And sometimes, using transfer learning can be a better choice than building a model from scratch.
Overall, this journey is still ongoing. I am still learning and improving, and I will keep updating this project as I explore more ideas in the future.
