---
layout: page
title: PySpark - Recommender System
description: ALS-based movie recommendation system with item-item collaborative filtering.
img: assets/img/th8.png
importance: 8
category: Data Science & Machine Learning
---

    Title: PySpark - Recommender System
    Description: ALS-based movie recommendation system with item-item collaborative filtering.. 
    Source code link: https://gitfront.io/r/ompranavagrawal/iyoZbxC7nE6z/PySpark-Recommender-System/

<div class="row"><h3>Introduction</h3></div>
<div class="row">
    This Markdown document encapsulates the implementation and findings of a Movie Recommender System developed. The system leverages Apache Spark's capabilities to predict movie ratings using the MovieLens 25M dataset. A hybrid approach, integrating ALS (Alternating Least Squares), item-item collaborative filtering, and supervised learning models, is employed to enhance recommendation accuracy and relevance.
</div><br>
<div class="row"><h3>Objective</h3></div>
<div class="row">
    The project aims to design a recommender system that predicts movie ratings by constructing a utility matrix and applying Alternating Least Squares (ALS). It evaluates the system using metrics such as RMSE (Root Mean Square Error), MSE (Mean Squared Error), and MAP (Mean Average Precision), and explores a hybrid model combining ALS, item-item collaborative filtering, and a supervised learning component.
</div><br>
<div class="row"><h3>Data Description</h3></div>
<div class="row">
    Utilizes the MovieLens 25M dataset, containing 25 million ratings across 62,000 movies, contributed by 162,000 users. This rich dataset serves as a benchmark for assessing the system's performance.
</div><br>
<div class="row"><h3>Methodology Overview</h3></div>
<div class="row">
    <ul>
    <li><b>Data Preprocessing</b>: Normalizes ratings by subtracting mean ratings to adjust for variance across movies.</li>
    <li><b>ALS Implementation</b>: Configures the ALS algorithm with hyperparameters tuning through cross-validation to predict ratings.</li>
    <li><b>Item-Item Collaborative Filtering</b>: Enhances prediction by calculating cosine similarity between movie pairs, leveraging user ratings.</li>
    <li><b>Supervised Learning Integration</b>: Incorporates movie and user features using a RandomForestRegressor, aiming to improve prediction accuracy.</li>
    <li><b>Hybrid Model Formation</b>: Combines predictions from ALS, item-item CF, and supervised models, adjusting their weights to optimize performance.</li>
    </ul>
</div><br>
<div class="row"><h3>Evaluation and Results</h3></div>
<div class="row">
    The system is thoroughly validated using RMSE, MSE, and MAP, showcasing the effectiveness of the hybrid approach. Weight distribution strategies are explored to fine-tune the model's performance, resulting in optimized recommendations.
</div><br>

<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/8_1.png" title="Parameter Scores vs Weights" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Parameter Scores vs Weights
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/8_2.png" title="Model Comparison" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Model Comparison
</div><br>

<div class="row"><h3>Conclusion</h3></div>
<div class="row">
   The report concludes that the integrated hybrid recommender system, utilizing Spark's MLlib, successfully predicts movie ratings on the MovieLens dataset. The combination of ALS, item-item collaborative filtering, and supervised learning demonstrates a significant improvement in prediction accuracy and recommendation quality.<br>
   For the detailed implementation, including code snippets and specific model evaluations, refer to the original Python code.

</div><br>
