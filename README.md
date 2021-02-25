# APITestFramework - ReadME

## About Framework
This framework is a Maven based project which is using Rest Assured to make API calls and its funtionality, TestNG has been used to Segragate and run Testcases. Extent Report has been used for reporitng strucure. Log4J has been used to put loggers in the TC which helps us to analyse the TC from logs perspective.

This suite can be executed by following ways.
1. From command prompt
    Go to folder \APITestFramework\APITestProject\
    open command prompt here
      run the command
      Command to Trigger API Automation Suite from cmd: mvn clean install -DsuiteFile="Reqres_TestNG.xml" -Denvironment="fasal"

2. From TestNG Classes
    Go to folder \APITestFramework\APITestProject\Reqres_TestNG.xml
    Run the Testcases using TestNG.xml
    
## Reports
Reports can be found at 
\APITestFramework\APITestProject\NewExtentReports\CompleteReport25-02-2021 11-24.html (Sample, All available reports will be avalable here. Latest can be used as correct reference of execution)

## Pre -requisite: 
Java should have been installed and Java Home, Path should have been set


# Framework Structure:
 ## src/main/java
  Here we have 
    common utilities and Base Class setting up driver
    Util class to access Environment and Data Properties
    Util class to to Fetch and Parse Date
    Class to define Header (If we have any new coming up, can be added here without any code changes)
    Listeneres to capture status and logs info to be added in extent report
    
 ## src/main/resource
    Here we have
      Data Propertties to define any data which can be used to run with different use cases
      Environment Properties- To ensure we just make minimal changes while running the same code in any other environment
      
 ## src/test/java
    Here We have
      Actual testcases which will be accessing common utils from /scr/main/java
      Any new TC would just need addition to this class or adding a new class with new features coming to the project
 ## src/test/resource
    Here we have
      We can have resources if we are using any other data for example, a data from CSV to be used in test Case
      
 ###  New Extent Report
    Here we have
      Reports of each run captured in a html file being saved with current date and time so that older reports are not being replaced
 
 ### test-output
    Here we have
      emailable reports
      
 ## pom.xml 
  Since this is Maven Based project all the jars and artifacts are being captured in Pom which will build the project and download all the jars
  
  ## Reqres_TestNG.xml
    This xml is the initiating source for TC execution and will contain the information about
      Testclasses and methods
      Environment
      
