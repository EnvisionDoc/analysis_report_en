# Sample Program - Embed Tableau Worksheet in Application
This sample project is used to demonstrate how to integrate worksheets developed by tableau desktop into business applications to realize single sign - on.

Before referring to this sample code, you need to understand [tableau related concepts](/devportal/index.html#/main/24/166/57baab5ed3eb4806104b045d/doccenter/Tableau/EN/1@Overview/Overview.md), and EnOS Tableau Server service [working mechanism](/devportal/index.html#/main/24/166/57baab5ed3eb4806104b045d/doccenter/Tableau/EN/1@Overview/Overview.md).

This project code is only for reference, please integrate it into the application according to actual needs.

## Prerequisites
To successfully use the sample project, you need the following:
1. [EnOS API SDK](/devportal/#/main/24/168/57baab5ed3eb4806104b045d/consoleMenu1) Version `0.1.47`
2. [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
3. [Maven 3](https://maven.apache.org/install.html)

## Sample Description
1. Sample scenario
- This example simulates a Web application, sending a request to the back-end service by clicking the button on the page. This allows the back-end service to send a request to the Tableau Server service to obtain the URL of the tableau worksheet. Finally, it displays the signed-in tableau worksheet page in an `iframe` at the front end.

2. Sample project framework
-  This sample project is developed using `JDK 1.8` and `Spring Boot 2.0`.
-  The back-end calls the interface that obtains the tableau URL through the application key,application secret in EnOS, application account registered in the tableau server service and the worksheet url in Tableau.
-  The front-end uses `jQuery` to call the interface in the back-end to obtain the tableau worksheet URL and display it in `iframe`.

## Procedure

1. [Download](/Documentation/Tableau/ZH/4@资源下载/tableauplugin-demo.zip) Sample App code.
2. Load Maven project after decompressing.
3. run the class and type in `localhost: 8080` in the browser to enter the following page.
  ![image](../PIC/sample_01.png)
4. Click the  **Report**  button. The application will load the tableau worksheet page in the form of `iframe`.
  ![image](../PIC/sample_02.png)
