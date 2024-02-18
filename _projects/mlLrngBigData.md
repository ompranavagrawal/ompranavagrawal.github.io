---
layout: page
title: PySpark - Machine Learning on Big Data
description: PySpark ML with TF-IDF, CrossValidator, ParamGrid, LogisticRegression, LinearSVC, RandomForestClassifier, MultilayerPerceptronClassifier.
img: assets/img/th10.png
importance: 10
category: Data Science & Machine Learning
---

    Title: PySpark - Machine Learning on Big Data
    Description: PySpark ML with TF-IDF, CrossValidator, ParamGrid, LogisticRegression, LinearSVC, RandomForestClassifier, MultilayerPerceptronClassifier. 
    Source code link: https://gitfront.io/r/ompranavagrawal/Nv5h64hkbadi/PySpark-Machine-Learning-on-big-data/

<div class="row"><h3>Introduction</h3></div>
<div class="row">
    This project aims to identify fake job postings within a dataset using PySpark, a powerful tool for handling big data. By employing different machine learning classifiers, we aim to develop a robust model that can accurately distinguish between genuine and fraudulent job listings.
</div><br>
<div class="row"><h3>Data Description</h3></div>
<div class="row">
    The dataset, "fake_job_postings.csv", consists of job listings with various attributes. Each listing is labeled as fraudulent or not, making this a binary classification problem.
</div><br>
<div class="row"><h3>Methodology</h3></div>
<div class="row"><h4>Data Preprocessing</h4></div>
<div class="row">
    <ul>
        <li><b>Data Loading</b>: The dataset is loaded from an HDFS path into a Spark DataFrame.</li>
        <li><b>Missing Value Analysis</b>: Columns with a significant percentage of missing values are identified and dropped.</li>
        <li><b>Text Cleaning</b>: Regular expressions are used to clean text columns, removing non-alphanumeric characters and converting text to lowercase.</li>
    </ul>
</div><br>
<div class="row"><h4>Feature Engineering</h4></div>
<div class="row">
    <ul>
        <li><b>Text Vectorization</b>: The description column is tokenized and vectorized using TF-IDF to transform textual data into a numerical format suitable for machine learning models.</li>
        <li><b>Data Balancing</b>: The dataset is balanced by undersampling the majority class to improve model performance on minority classes.</li>
    </ul>
</div><br>


<div class="row"><h4>Model Training and Evaluation</h4></div>
<div>
    Four classifiers are evaluated:
    <ol>
        <li><b>Logistic Regression</b></li>
        <li><b>Linear Support Vector Classifier (LinearSVC)</b></li>
        <li><b>Random Forest Classifier</b></li>
        <li><b>Multilayer Perceptron Classifier</b></li>
    </ol>
    For each model:
    <ul>
        <li>A Pipeline is constructed, including preprocessing and the classifier.</li>
        <li>Hyperparameter tuning is performed using CrossValidator with a ParamGridBuilder.</li>
        <li>Model performance is assessed using accuracy and F1 score.</li>
    </ul>
</div><br>
<div class="row"><h3>Results</h3></div>
<div class="row">
   Model performance is documented, detailing the accuracy, F1 score, and best parameters for each classifier.
</div><br>

<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/10_1.png" title="Logistic Regression" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Logistic Regression
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/10_2.png" title="Multi Layer Perceptron" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Multi Layer Perceptron
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/10_3.png" title="Random Forest Classifier" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Random Forest Classifier
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/10_4.png" title="Linear Support Vector Classifier" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Linear Support Vector Classifier
</div><br>

<div class="row"><h3>Conclusion</h3></div>
<div class="row">
   The project demonstrates the application of various machine learning models to detect fake job postings in a big data environment using PySpark. The effectiveness of each model varies, with detailed results providing insights into the best-performing models based on accuracy and F1 score.
</div><br>
