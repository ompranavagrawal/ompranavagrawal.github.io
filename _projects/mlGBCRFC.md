---
layout: page
title: PySpark - Machine Learning with Gradient Boost and Random Forest Classifier
description: PySpark ML with TF-IDF, CrossValidator, ParamGrid, DecisionTreeClassifier, RandomForestClassifier, GBTClassifier, MultilayerPerceptronClassifier.
img: assets/img/th7.png
importance: 7
category: Data Science & Machine Learning
---

    Title: PySpark - Machine Learning with Gradient Boost and Random Forest Classifier
    Description: PySpark ML with TF-IDF, CrossValidator, ParamGrid, DecisionTreeClassifier, RandomForestClassifier, GBTClassifier, MultilayerPerceptronClassifier.
    Source code link: https://gitfront.io/r/pranav/AGyTKh2Lq4kd/PySpark-Machine-Learning-with-Gradient-Boost-and-Random-Forest-Classifier/
    Video Link: https://youtu.be/G-MCYTs8FpQ

<div class="row"><h3>Introduction & Methods</h3></div>
<div class="row">
    This report investigates the impact of ensemble methods, specifically bagging and boosting, on machine learning models, using a flight data delay dataset. It compares these methods against a neural network model, emphasizing data preparation, model training, and validation across various metrics.
</div><br>
<div class="row"><h3>Data Description</h3></div>
<div class="row">
    The report utilizes the Air Flight Dataset, detailing flight records, cancellations, and delays per airline from January 2018, derived from the TranStats "On-Time" database.
</div><br>
<div class="row"><h3>Architecture</h3></div>
<div class="row">
    The study employs PySpark libraries, focusing on a Decision Tree, Multi-Layer Perceptron neural network, Gradient Boosting, and Random Forest classifiers. It outlines the code architecture and pseudo-code for data cleaning, balancing, preprocessing, and model training.
</div><br>
<div class="row"><h3>Data Preprocessing</h3></div>
<div class="row">
    Describes the steps taken for redundant column removal, binary recoding of delay and cancellation indicators, normalization of textual data, and balancing the dataset through undersampling.
</div><br>
<div class="row"><h3>Results</h3></div>
<div class="row">
    Presents detailed results of model training and evaluation for DecisionTreeClassifier, MultiLayerPerceptronClassifier, RandomForestClassifier, and GBTClassifier, including hyperparameter tuning and the effects on accuracy, F1 scores, and ROC-AUC.
</div><br>

<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/7_1.png" title="Decision Tree Classifier Evaluation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Decision Tree Classifier Evaluation
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/7_2.png" title="Multi Layer Perceptron Evaluation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Multi Layer Perceptron Evaluation
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/7_3.png" title="Random Forest Classifier Evaluation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Random Forest Classifier Evaluation
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/7_4.png" title="Gradient Boosted Tree Evaluation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Gradient Boosted Tree Evaluation
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/7_5.png" title="Performance Comparison of Different Classifier" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Performance Comparison of Different Classifier
</div><br>

<div class="row"><h3>Conclusion</h3></div>
<div class="row">
   The study concludes that ensemble methods, particularly bagging and boosting, outperform the neural network model in predicting flight delays, with significant improvements in accuracy and stability. It highlights the importance of thorough data preparation and model optimization.
</div><br>
