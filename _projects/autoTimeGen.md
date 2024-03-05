---
layout: page
title: Automated Timetable Generator
description: An application of Genetic Algorithm
img: assets/img/th1.png
importance: 1
category: Software Engineering
---
    
    Title: Automated Timetable Generator using Genetic Algorithm 
    Source code link : https://github.com/ompranavagrawal/Automated-Timetable-Generator-using-Genetic-Algorithm

<div>
    <div><h3>Abstract</h3></div>
    <div>Automatic Timetable Generator is a Java based application used to generate timetable automatically. Currently timetable is managed manually. It will help  to manage all the  periods automatically and also will be helpful for faculty to get  timetable by using application. It will also manage timetable when  any teacher is absent , late coming or early going. Maximum and minimum work  load for a Faculty for a day, week and  month will be specified  for  the efficient generation of timetable.</div><br>
    <div><h3>Introduction</h3></div>
    <div>Time table scheduling has been in human requirements since they thought of managing time eﬀectively. It is widely used in schools, colleges and other fields of teaching and working like crash courses, couching centres, training programs etc . In early days, time table scheduling was done manually with a single person or some group involved in task of scheduling it with their hands, which take lot of eﬀort and time.</div><br>
    <div>While scheduling even the smallest constraints can take a lot of time and the case is even worse when the number of constraints or the amount of data to deal with increases. In such cases perfectly designed time table is reused for whole generation without any changes, proving to be dull in such situations. Other cases that can cause problem is when the number of employers/workers are weak, resulting in rescheduling of time table or they need to ﬁll on empty seats urgently.</div><br>
    <div>Institutions/Schools/Collages/Universities are the regular users of such time tables. They need to schedule their course to meet the need of current duration and facilities that are available to them. However, their schedule should meet the requirement of new course addition and newly enrolled students to fresh batches. This may result in rescheduling the entire time table once again for its entire batches and to be scheduled in shortest possible time before the batches course start. Another problem that occur when scheduling time table for exams. When multiple batches have exam on same day, they need to be schedules eﬀectively taking into account all problems related to facilities that are available to conduct these exams simultaneously.</div><br>
    <div><h3>Benefits</h3></div>
    <div>Automated Timetable Generator, our software allows users to generate time table for newly occurring changes in less time, with less eﬀort and with more eﬃciency. It will allow users to work on and view time tables in diﬀerent platforms and view diﬀerent information simultaneously.</div><br>
    <div class="row">
        <div class="mt-3 mt-md-0 mx-auto">
            {% include figure.liquid path="assets/img/1_1.png" title="Use Case Diagram" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        Use Case Diagram
    </div><br>
    <div class="row">
        <div class="mt-3 mt-md-0 mx-auto">
            {% include figure.liquid path="assets/img/1_2.jpeg" title="Work Breakdown Structure" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
            Work Breakdown Structure
    </div><br>
    <div><h3>Algorithm Implementation</h3></div>
    <div>TimeTable generation is an NP-Complete problem; speciﬁcally speaking NP-Hard. So it lacks a proper time bound for execution i.e. problems like these often can have many diﬀerent outputs. So we assign cost to each output which gives the measure of deviation of the output from the desired one. So our aim is to get the output with minimum cost if there is one.</div><br>
    <div>Genetic algorithm can give best results but the time needed for it to compute cannot be determined so we have developed an alternative approach which can be applied to solve most of the NP-Complete problems.</div>
    <div><ul><li>First determine the various constraints which the output must satisfy.</li>
        <li>We then categorize them as soft and hard constraints. </li>
        <li>Third step is to make a procedure which can generate an output for most of the possible inputs. </li>
        <li>The ﬁnal step is to reduce the cost.</li></ul></div>
    <div>The current working scenarios these can be explained as follows. The ﬁrst two steps are explained earlier. The procedure mentioned in the third step here is the gene() function in the TimeTableGA class. What this function does is to assign properties to teacher, subject and position. So that if we arrange timetable according to this priority there is a greater probability to end up in the output which satisﬁes all the hard constraints.</div><br>
    <div>First and foremost priority is that of teachers. Subject priority and position priority depends on teacher priority, also teacher is the most important resource in the time table. The priority of teacher increases if the number of periods he handled increases, also if the number of  batches he is present increases and decreases if an alternative teacher is available. Subject priority is also similar to that of teacher priority. It must also increase with the continuous hours needed. So in the algorithm we have considered subject which have diﬀerent consecutive periods need as diﬀerent subjects. Position has priority if it correctly ﬁts and the adjacent portions are not that of the same subject.</div><br>
    <div>Finally we need to manually assign priority and optimize the table to reduce cost. The main logic of our algorithm resides in the TimetableGA class. The gene function in the class reads the various data needed for generation of timetable for current batches from the GUI  creates the table in an String and copies it back .</div><br>
    <div class="row">
        <div class="mx-auto mt-3 mt-md-0">
            {% include figure.liquid path="assets/img/1_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        Login Form
    </div><br>
    <div class="row">
        <div class="mx-auto mt-3 mt-md-0">
            {% include figure.liquid path="assets/img/1_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        Data Entry Form
    </div><br>
    <div class="row">
        <div class="mx-auto mt-3 mt-md-0">
            {% include figure.liquid path="assets/img/1_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        TimeTable Name Entry
    </div><br>
    <div class="row">
        <div class="mx-auto mt-3 mt-md-0">
            {% include figure.liquid path="assets/img/1_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        Sample output
    </div><br>
    <div><h3>Testing</h3></div>
    <div>Testing is an important phase in software lifecycle. Testing improves reliablity and robustness of the application. The basic operations to be tested are</div>
    <div><ul>
            <li>There should be at least one working day and one working hour.</li>
            <li>Diﬀerent inputs must be checked for its range. For example no of hours in morning or evening should be between 0-5, total number of periods for a course must be between 0-70, code for course must be 0-8 character long.</li>
            <li>User should not be given permission to edit or modify subjects, teachers or batches without releasing its associations </li>
            <li>Before generating table it should be checked if all subjects are assigned at least one teacher, no of periods available((morning hours +evening hours)*no of days) must be equal to no of periods assigned.</li>
            <li>If any problem occurs during generation (due to constraints) it must be properly displayed.</li>
        </ul>
    </div><br>
    <div><h3>Test Approach</h3></div>
    <div>The system is to be tested at various stages of the project development: Each user interface is tested individually for its function. Interfaces meant for data input are tested by entering data in the data tables through each interface. Similarly each data base operation is tested through interfaces.</div><br>
    <div>All the user interfaces are joined in the desired sequence and their back end coding is tested for the desired result. Like previous window close as the next desired window opens and each button performs its desired task etc.</div><br>
    <div>Every class in the java code is tested individually with the help of test cases. Whole of the algorithm is tested with sample run of data to generate an optimal time table for the provided database.</div><br>
    <div><h3>Test Planning</h3></div>
    <div>Most of the testing requires checking connectivity of the user interfaces, so a properly designed text file is required for testing. Design interfaces and connect each of them to the database and test them for proper output as is it is in the database.</div><br>
    <div>Inter connect all the user interfaces in the desired sequence. Check if each of the buttons result in the desired result. Develop the java classes for data retrieval. Test each of them according to test cases. Develop java code for timetable generation. Test the coding with a small database by generating a time table.</div><br>
    <div><h3>Functional Test Criteria</h3></div>
    <div>The objective of these test is to ensure that each element of the application meets the functional requirement of the user.
    <ul><li>Requirements Catalogue</li>
        <li>Other functional documents produced during the course of the project i.e. resolution to issues/change requests/feedback. </li>
        <li>Validation Testing - which is intensive testing of the new Front end ﬁelds and screens. Windows GUI Standards; valid, invalid and limit data input; screen look and appearance, and overall consistency with the rest of the application.</li>
        <li>Functional testing - these are low-level tests which aim to test the individual processes and data ﬂows.</li>
    </ul>
    </div><br>
    <div><h3>Integartion Testing</h3></div>
    <div>This test proves that all areas of the system interface with each other correctly and that there are no gaps in the data ﬂow. Final Integration Test proves that system works as integrated unit when all the ﬁxes are complete.</div><br>
    <div><h3>User Acceptance Test</h3></div>
    <div>This test, which is planned and executed by the User Representative(s), ensures that the system operates in the manner expected, and any supporting material such as procedures, forms etc. are accurate and suitable for the purpose intended. It is high level testing, ensuring that there are no gaps in functionality.</div><br>
    <div><h3>System Test Criteria</h3></div>
    <div>Entrance Criteria: <ul><li>All developed code must be unit tested. Unit and Link Testing must be completed and signed oﬀ by development team.</li>
        <li>All human resources must be assigned and in place. • All test hardware and environments must be in place, and free for System test use.</li>
    </ul>Exit Criteia: <ul><li>All High Priority errors from System Test must be ﬁxed and tested</li></ul></div><br>
    <div><h3>Test cases and Test results</h3></div>
    <div>Outlined below are the main test types that are performed for this release. All test entries on wrong input has been tested to verify code stablilty and correctness. The test cases presented here are based on criterias presented above to validate its test implementation. Each test case table list the detailed test case results for each interface and its user inputs that can be assinged by the user to check the correctness of its implematation.</div><br>
</div>    


