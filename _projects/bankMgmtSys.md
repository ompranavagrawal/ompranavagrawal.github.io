---
layout: page
title: Bank Management System
description: Application based on Python with Oracle 11g.
img: assets/img/th4.jpg
importance: 4
category: Software Engineering
---


    Title: Bank Management System
    Description: Application based on Python with Oracle 11g.
    Source code link: https://github.com/ompranavagrawal/Bank-Management-System.git

<div class="row"><h3>Introduction</h3></div>
<div class="row">
    Certified by Infosys Limited, developed a comprehensive application built with Java and Spring Framework and an MS SQL database for robust management of checking and savings accounts, as well as debt management operations.
</div><br>
<div class="row"><h3>Description</h3></div>
<div class="row">
    This code is a Python script that simulates a basic banking system, utilizing the cx_Oracle library to interact with an Oracle database and the tabulate library to format output tables. It supports several operations:
    <ul><li><b>Sign Up</b>: Allows new users to create an account by entering details such as account type, holder name, address, password, and initial deposit amount. It inserts these details into a database table and generates unique customer and account numbers.</li>
    <li><b>Address Change</b>: Enables users to update their address information in the database for a given account number.</li>
    <li><b>Money Deposit</b>: Allows users to deposit money into their account. It updates the balance in the database after adding the deposited amount to the current balance.</li>
    <li><b>Money Withdrawal</b>: Enables users to withdraw money from their account if they have sufficient balance. It also updates the balance in the database.</li>
    <li><b>Print Statement</b>: Generates a statement of transactions within a specified date range for a given account number, displaying the date, transaction type, and balance.</li>
    <li><b>Transfer Money</b>: Allows users to transfer money from their account to another account if they have sufficient balance and the receiver account exists.</li>
    <li><b>Account Closure</b>: Marks an account as closed and records the closure date in the database.</li>
    <li><b>Fixed Deposit</b>: Users can create a fixed deposit account with a minimum amount and term.</li>
    <li><b>Loan Management</b>: Users can apply for a loan if they are eligible (based on their balance and existing loan amount) and view loan details.</li>
    <li><b>Admin Sign In</b>: Special functionality for admins to view reports and perform administrative tasks.</li>
    <li><b>Opening New Accounts</b>: Users can open additional saving, current, or fixed deposit accounts.</li>
    <li><b>Main Menu and Sign In</b>: The script provides a main menu for navigation and allows existing users to sign in and perform banking operations.</li></ul>
</div>
<div class="row">The script uses procedural programming to define functions for each feature and interacts with a database using SQL queries for data manipulation and retrieval. Each operation requires user input for various details, and the system provides feedback based on the actions performed.</div><br>

