---
layout: page
title: Student Survey Application
description: An application of Spring Boot based web services with JPA, Angular and Docker.
img: assets/img/th2.png
importance: 2
category: Software Engineering
giscus_comments: true
---

    Title: Student Survey Application
    Description: An application of Spring Boot based web services with JPA, Angular and Docker.
    Source code link: https://gitfront.io/r/pranav/EnGL3jprcxGx/student-Survey-Application/
    Video link: https://youtu.be/MwEHHcC--Qw


<div class="row"><h3>Description</h3></div>
<div class="row">
    This project is a web-based survey system designed for prospective students visiting a university campus. It utilizes a three-tier architecture, integrating frontend, backend, and database technologies. The frontend is developed using Angular, offering a user-friendly interface for survey submission and displaying results. The backend is built with RESTful Web Services, employing Spring Boot for handling data interactions, either through JDBC or JPA. The database tier stores survey-related information. Additionally, Docker containerization is applied to encapsulate both frontend and backend components, ensuring efficient deployment and scalability.
</div><br>

<div class="row"><h3>Components</h3></div>
<div class="row">
    Key functionality classes and components used in the web-based survey system:
    <ul>
        <li>
            <b>SurveyFormController</b>: A Spring MVC controller that manages survey form submissions. It handles HTTP requests for displaying the survey form and submitting survey data.
        </li>
        <li>
            <b>SurveyService</b>: A service layer component that abstracts the business logic for survey operations. It interacts with the data layer to fetch or persist survey data.
        </li>
        <li>
            <b>SurveyRepository</b>: An interface for data access operations on survey entities. It leverages Spring Data JPA to simplify database interactions.
        </li>
        <li>
            <b>Survey</b>: An entity class representing the survey data model. It includes fields such as survey id, participant name, answers to questions, and timestamps.
        </li>
        <li>
            <b>Docker</b>: Used to containerize the application, making it easier to deploy and scale. The report details how Docker images for both the frontend and backend are created and managed.
        </li>
        <li>
            <b>Angular Components</b>: The frontend utilizes Angular components to create a dynamic and responsive user interface. These components include forms for survey submission and views for displaying survey results.
        </li>
        <li>
            <b>Security Configuration</b>: The application employs Spring Security to ensure secure access to the survey system. It configures authentication and authorization for different parts of the application.
        </li>
    </ul>
</div>
<div class="row">
    These components work together to create a comprehensive system for conducting surveys among prospective students, ensuring ease of use, data integrity, and scalability.
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/2_1.png" title="Use Case Diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Homepage
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/2_2.png" title="Work Breakdown Structure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        Survey Form
</div><br>
<div class="row">
    <div class="mt-3 mt-md-0 mx-auto">
        {% include figure.liquid path="assets/img/2_3.png" title="Work Breakdown Structure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
        List all Survaye Page
</div><br>

