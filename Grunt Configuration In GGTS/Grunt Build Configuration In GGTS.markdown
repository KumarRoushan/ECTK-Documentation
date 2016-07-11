# Grunt Configuration in GGTS #

In order to make any changes in ECTK UI files, such as, html, AngularJs and in CSS files needs to be minified to render the changes in browser.

We can achieve the changes by using the the below manual steps.

*    Open gitbash from Grunt.js location in codebase
*    Type grunt prod command on the command prompt, where prod is the grunt task.

The above steps need the manual intervention in running the command on every changes to render in the browser.

To sreamline and automate this process, we can hookup the grunt in GGTS automatic build process. Follow the below steps to achieve the same.


Application Name: **ECTK**

**Version: 1.0**

Version Date: 11th July 2016

Version Control

Version | Date          | Comment
--------| ------------- | ---------------
1.0     | 11th Jul 2016 | Initial Content describes the grunt configuration in GGTS.
        |               | 
</br>

#Steps#

1.	Click on **Project -> Properties** menu in GGTS.
2.	Click on **Builder -> New**
3.	Type **C:\Windows\System32\cmd.exe** in Location text box.
4.	Type **Gruntfile.js** location in Working Directory text box.
5.	Type **/c grunt prod & exit** in Argument text box. 
6.	Make sure you have selected **During auto builds** option alone in **Build Option** tab.
7.	Click on **Apply** and **OK**

<br>
Find below the screen shot for your reference.

<img src="GruntInGGTS_1.jpg" alt="Grunt Configuration in GGTS First Image" style="align:left; width:100%">

<img src="GruntInGGTS_2.jpg" alt="Grunt Configuration in GGTS First Image" style="align:left; width:100%">


Thanks