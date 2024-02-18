---
layout: page
title: Iris and Digits Clustering using K-Means
description: Clustering data using the K-Means algorithm, focusing on minimizing centroid distances to improve cluster quality.
img: assets/img/th11.png
importance: 11
category: Data Science & Machine Learning
---

    Title: PySpark - ris and Digits Clustering using K-Means
    Description: Clustering data using the K-Means algorithm, focusing on minimizing centroid distances to improve cluster quality.
    Source code link: https://github.com/ompranavagrawal/Iris_and_Images_Clustering_using_kMeans.git

<div class="row"><h3>Objective</h3></div>
<div class="row">
    The project aims to accurately cluster data using the K-Means algorithm, focusing on minimizing centroid distances to improve cluster quality.
</div><br>
<div class="row"><h3>Preprocessing</h3></div>
<div class="row">
    Data normalization and image smoothing techniques, including Gaussian smoothing, were employed to enhance clustering performance.
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/11_1.png" title="Gaussian smoothing" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Gaussian smoothing for noise removal
</div><br>
<div class="row"><h3>Dimensionality Reduction</h3></div>
<div class="row">
    Truncated SVD and t-SNE were used for reducing dimensions, alongside MinMaxScaler for feature scaling, to prepare data for clustering.
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/11_2.png" title="Clustering" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Clustering
</div><br>
<div class="row"><h3>K-Means Algorithm Application</h3></div>
<div class="row">
    <ul>
        <li>Initial centroids were chosen from data points to avoid bad initializations.</li>
        <li>The Euclidean distance was used for assigning data points to the nearest centroid.</li>
        <li>The process iterated until k centroids were determined, optimizing cluster quality.</li>
    </ul>
</div><br>
<div class="row"><h3>Observations</h3></div>
<div class="row">
    <ul>
        <li>Choosing centroids from data points yielded better results.</li>
        <li>Optimal clustering for the Iris dataset was achieved with 3 clusters, as indicated by silhouette scores and inertia calculations.</li>
        <li>For the Digits dataset, 10 clusters provided the best silhouette scores, indicating optimal clustering.</li>
    </ul>
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/11_3.png" title="Inertia and Silhouette score for Iris" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Inertia and Silhouette score for Iris
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/11_4.png" title="Inertia and Silhouette score for Image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
       Inertia and Silhouette score for Image
</div><br>
<div class="row"><h3>Conclusion</h3></div>
<div class="row">
    K-Means clustering effectively labeled the Iris and Digits datasets, demonstrating the algorithm's capability to manage and cluster large datasets efficiently.
</div><br>