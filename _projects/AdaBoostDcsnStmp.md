---
layout: page
title: Adaboost Using Decision Stump
description: Adaboost algorithm implementation using Decision Stumps as weak learners to classify a dataset with improved accuracy.
img: assets/img/th12.png
importance: 12
category: Data Science & Machine Learning
---

    Title: Adaboost Using Decision Stump
    Description: Adaboost algorithm implementation using Decision Stumps as weak learners to classify a dataset with improved accuracy.
    Source code link: https://github.com/ompranavagrawal/AdaboostUsingDecisionStump.git

<div class="row"><h3>Objective</h3></div>
<div class="row">
    The goal is to implement the Adaboost algorithm using Decision Stumps as weak learners to classify a dataset with improved accuracy. Decision Stumps are one-level Decision Trees that use a single attribute to make a decision, making them perfect for use as weak learners in the Adaboost algorithm.
</div><br>
<div class="row"><h3>Implementation Details</h3></div>
<div class="row"><h4>Dataset Preparation</h4></div>
<div class="row">
    The dataset is first preprocessed to ensure it is suitable for training and testing the Adaboost model. This involves cleaning, normalization (if necessary), and splitting the dataset into training and testing sets.
</div><br>
<div class="row"><h4>Decision Stump as Weak Learner</h4></div>
<div class="row">
    <ul>
        <li><b>Decision Stump Implementation</b>: Each decision stump is implemented to select the best threshold for splitting the data based on the Gini Index. This involves evaluating every feature in the dataset to determine the best split.</li>
        <li><b>Feature Selection</b>: The algorithm iteratively considers each feature in the dataset, calculating the Gini Index for different splitting points to find the feature and threshold that provide the best split.</li>
    </ul>
</div><br>
<div class="row"><h4>Adaboost Algorithm</h4></div>
<div class="row">
    <ul>
        <li><b>Initialization</b>: Initialize weights for each instance in the dataset equally.</li>
        <li><b>For each iteration:</b>:
            <ul>    
                <li>Train a decision stump using the current weights.</li>
                <li>Calculate the stump's error rate: The error is measured based on how well the stump performs on the weighted dataset.</li>
                <li>Compute the stump's weight in the final classification: This is based on the stump's error rate, with more accurate stumps receiving higher weights.</li>
                <li>Update weights for each instance: Increase weights for incorrectly classified instances and decrease for correctly classified ones, ensuring that subsequent stumps focus more on difficult cases.</li>
                <li>Normalize weights to ensure they sum up to 1.</li>
            </ul>
        </li>
        <li><b>Final Model</b>: Combine the decision stumps into a weighted sum that represents the final model.</li>
    </ul>
</div><br>

<div class="row"><h4>Parameter Tuning</h4></div>
<div class="row">
    The number of decision stumps is a critical parameter. The implementation tests the performance of the Adaboost model with a varying number of stumps to find the optimal count that minimizes error without leading to overfitting.
</div><br>

<div class="row"><h4>Results and Observations</h4></div>
<div class="row">
    The implementation showcased that as the number of decision stumps increased, the model's ability to classify the training data improved, with diminishing returns and eventual overfitting beyond an optimal point. This optimal range of stumps provided the best balance between bias and variance, leading to improved generalization on unseen data compared to a single decision tree.
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/12_1.png" title="Boosting vs Error Graph" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Boosting vs Error Graph
</div><br>
<div class="row"><h4>Conclusion</h4></div>
<div class="row">
    The implementation of the Adaboost algorithm using Decision Stumps as weak learners demonstrated significant improvements in prediction accuracy over a baseline decision tree model. By carefully tuning the number of stumps, it is possible to achieve a robust model that generalizes well to new data, showcasing the power of ensemble learning techniques in machine learning.
</div><br>
