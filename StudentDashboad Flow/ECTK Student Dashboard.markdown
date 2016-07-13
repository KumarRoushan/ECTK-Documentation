# ECTK Student Dashboard Flow #

This document explains the student dashboard technical flow. It also explains about the required js, html and database flow.

This document will be keep on updated based on our findings in ECTK technical flow of various functionalies. Below version control will highlights our finding in document.
 
Application Name: **ECTK**

**Version: 1.2**

Version Date: 13th July 2016

Version Control

Version | Date          | Comment
--------| ------------- | ---------------
1.0     | 8th Jul 2016  | Initial Content describes the dashboard flows from User interface to service layer, model and databases. <br> Worth to mention here that application does contain any DAO layer rather service layer is contains Transactional services and plays the significant roles in creating criteria queries. Models contains the DAO logics.
1.1     | 11th Jul 2016 | Updated diagram for getting the dashboard landing page details, such as, video, essentials etc using **dashboardService.js**
1.2     | 13th Jul 2016 | Added Alert and Notification flow and updated the **Student Dashboard Flow** diagram by moving out the notification flow in saperate diagram. 

</br>

Below diagram is self explanatory which decribes the required layers and flow of getting the details during the first time rendring the student dashboard page. 

<img src="Dashboard Flow.png" alt="ECTK Student Dashboard Flow" style="align:left; width:150%">

**Dashboard Landing and EC Scheduling Page**

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

**Notification and Alert Flow**

Below diagram depicts the Alert and Notification flow. Notification hits the backend service on every 5 minutes to get the updated notification message.

<img src="Notification And Alert Flow.png" alt="ECTK Student Dashboard Flow" style="align:left; width:170%">

**Data Modelling**

Below tables and respective columns are involved in Student Dashboard flow.

Table Name         | Columns       | Comment
-----------------  | ------------- | ----------------
Student_Dashboard  | Elective Period,<br> Essentials_JSON,<br> FAQ_JSON, <br> Links_JSON,<br> Video_JSON | All the data related to landing page comes from this table.
Student_Requests   | Student,<br>Requests_JSON | All the details related to students source selection/My Priorities details comes from this table.
Notification       |Id, <br> Code, <br> Default_Message, Code, Type,<br> Person, <br>Elective Period | This table joins the Person, Elective_Period and Notification_Args tables to get the various details.


