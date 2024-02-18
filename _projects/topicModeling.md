---
layout: page
title: PySpark - Topic Modeling
description: Incorporating Topic Modeling using LDA to enhances tweet sentiment classification accuracy.
img: assets/img/th9.png
importance: 9
category: Data Science & Machine Learning
---

    Title: PySpark - Topic Modeling
    Description: Incorporating Topic Modeling using LDA to enhances tweet sentiment classification accuracy.
    Source code link: https://gitfront.io/r/ompranavagrawal/y6MLKJhzSJRn/PySpark-Topic-Modeling/

<div class="row"><h3>Objective</h3></div>
<div class="row">
    The goal is to assess the impact of Topic Modeling on the accuracy of tweet sentiment classification. It involves comparing the performance of sentiment classification using TFIDF vectors with and against LDA-derived features, employing logistic regression and cross-validation in pySpark, and visualizing results with pyLDAvis.
</div><br>
<div class="row"><h3>Data Description</h3></div>
<div class="row">
    The dataset comprises approximately 1.727 million tweets from the "US Election 2020 Tweets" dataset on Kaggle. It serves to analyze Twitter sentiment's correlation with US Presidential Election outcomes, exploring social media's influence on political processes.
</div><br>
<div class="row"><h3>Methodology</h3></div>
<div class="row"><h4>Data Preprocessing</h4></div>
<div class="row">
    <ul>
        <li><b>Loading Data</b>: Tweets are read from a CSV file into a DataFrame.</li>
        <li><b>Filtering and Cleaning</b>: Tweets are filtered to include only those with English alphabet characters, followed by sentiment analysis to classify tweets into positive or non-positive sentiments.</li>
        <li><b>Tokenization and Stop Words Removal</b>: Tweets are tokenized, and stop words are removed.</li>
    </ul>
</div>
<div class="row"><h4>LDA Implementation</h4></div>
<div class="row">
    <ul>
        <li><b>Feature Transformation</b>: Uses CountVectorizer to convert tokens into feature vectors.</li>
        <li><b>Model Setup and Training</b>: An LDA model is initialized to discover underlying topics within tweets, with the Spark ML Pipeline facilitating model fitting and transformation.</li>
    </ul>
</div>
<div class="row"><h4>Visualization and Classification</h4></div>
<div class="row">
    <ul>
        <li><b>Visualization</b>: Utilizes pyLDAvis for an interactive visualization of the topics discovered by the LDA model.</li>
        <li><b>Classification with Logistic Regression</b>: Employs logistic regression models, first with TFIDF vectors and then enhanced by LDA topic distribution features, to classify tweet sentiments. The models are evaluated based on accuracy, F1 score, and area under the ROC curve.</li>
    </ul>
</div>

<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/9_1.png" title="pyLDAvis Visualization" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       pyLDAvis Visualization
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/9_2.png" title="Model Comparison" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Model Comparison
</div><br>

<div class="row"><h3>Results and Conclusion</h3></div>
<div class="row">
    The integration of LDA topic probabilities with TFIDF vectors improved sentiment classification accuracy, demonstrating that combining thematic context with traditional text vectorization benefits sentiment analysis tasks by providing a more comprehensive data understanding.
</div><br>
