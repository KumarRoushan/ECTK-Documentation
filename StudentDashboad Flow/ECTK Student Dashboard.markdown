# ECTK Student Dashboard Flow #

This document explains the student dashboard technical flow. It also explains about the required js, html and database flow.

This document will be keep on updated based on our findings in ECTK technical flow of various functionalies. Below version control will highlights our finding in document.
 
Application Name: **ECTK**

**Version: 1.1**

Version Date: 11th July 2016

Version Control

Version | Date          | Comment
--------| ------------- | ---------------
1.0     | 8th Jul 2016  | Initial Content describes the dashboard flows from User interface to service layer, model and databases. <br> Worth to mention here that application does contain any DAO layer rather service layer is contains Transactional services and plays the significant roles in creating criteria queries. Models contains the DAO logics.
</br>

Below diagram is self explanatory which decribes the required layers and flow of getting the details during the first time rendring the student dashboard page. 

<img src="Dashboard Flow.png" alt="ECTK Student Dashboard Flow" style="align:left; width:200%">

**User Interface**

ECTK UI is based on AngularJs and maintains it's own MVC pattern in order to make the controller call and injects the service layer to make the various calls to backend.

In context to ECTK, AngularJs structures the UI in template pattern. It helps in defining the modular structure of UI. Below files are involved in drwaing the stundent dashboad UI.

*    Student.js
*    NavbarCtrl.js
*    initService.js
*    ecCatalogCard.html
*    ectPriorityList.html
*    ectPriorityListCard.html
*    ectCalendar.html
*    ectCalendarCard.html

<br>
**Data Modelling**

Below tables and respective columns are involved in Student Dashboard flow.

Table Name         | Columns       | Comment
-----------------  | ------------- | ----------------
Student_Dashboard  | Elective Period,<br> Essentials_JSON,<br> FAQ_JSON, <br> Links_JSON,<br> Video_JSON | All the data related to landing page comes from this table.
Student_Requests   | Student,<br>Requests_JSON | All the details related to students source selection/My Priorities details comes from this table.
Notification       |Id, <br> Code, <br> Default_Message, Code, Type,<br> Person, <br>Elective Period | This table joins the Person, Elective_Period and Notification_Args tables to get the various details.


