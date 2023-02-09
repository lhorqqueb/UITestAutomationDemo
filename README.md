# UI Test Automation Framework
Production ready UI Test Automation Framework based on Selenium WebDriver and TestNG. This lightweight test framework utilizes abstracted UI user elements and produces extent HTML test report.

## I would love to showcase the framework in detail, please contact me for a demo.

## Dependencies
This project depends on the following external libraries.

* **selenium-java**: Browser automation code
* **webdrivermanager**: managing driver binaries through code
* **testng**: creating and managing test cases
* **extentreport**: generating HTML based test execution report
* **javafaker**: generating randomized test data on the fly


## Framework Project Structure Diagram
```text
|-reports               #contains test report generated
|-src
   |-test
       |-java
           |-[+]base    # all the parent class is organized here
           |-[+]pages   # all the page object class is organized here
           |-[+]tests   # all the test class is organized here
           |-[+]util    # all the commonly used class is organized here
|-gitignore              # add git ignore file config here
|-pom.xml                # maven project config file
```
![screenshot](/images/ProjectStructure.png)

## Pre-requisites
* Download and isntall Chrome, Firefox, and Edge browser
* Download and install [JDK v1.8+](https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html)
* Download and install [[Apache Maven v3.0+](https://maven.apache.org/download.cgi)]
* Download and install [Git v2.0+](https://git-scm.com/downloads)

## Internal Framework Structure
This is a diagram that details the internal structure of this framework.
![screenshot](/images/FrameworkStructure.jpeg)


## How to Run Tests
All the tests triggering is conducted by **`mvn`** command, this framework supports test execution by multiple different browsers.


#### Supported Browsers:
| Browser   | Maven Options        |
|-----------|----------------------|
| Chrome    | `-Dbrowser=chrome`   |
| FireFox   | `-Dbrowser=firefox`  |
| MS Edge   | `-Dbrowser=edge`     |
| Headless  | `-Dbrowser=headless` |

To Trigger all the test case executions:
```shell
mvn test
```
To Trigger all the test grouped as `smoke`:
```shell
mvn test -Dgroups=smoke
```
To Trigger all or specified test with desired browser:
```shell
mvn test -Dbrowser=chrome
mvn test -Dbrowser=chrome -Dgroups=smoke
```

## How to View Report
All the test execution report will be saved on the `reports` folder.
```text
|-reports
   |-Index.html
```

Please navigate to this folder to view the test exception result, sample ExtentReport will look like this with more test cases. [Reference](https://www.extentreports.com/docs/v5/wiki/spark/spark.html#)
![screenshot](/images/ExtentReportSS.png)



