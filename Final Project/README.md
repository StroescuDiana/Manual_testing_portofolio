# Practice Project Manual Testing

The scope of the final project for ITF Manual Testing Course is to use all gained knowledge through the course and apply them in practice, using a live application. 

Application under test: https://demo.opencart.com/

API Documentation: https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md

**The final project will be split into 2 sections: [Testing section](https://github.com/StroescuDiana/manual_testing_portofolio/tree/main/Final%20Project#1-testing-section) and [SQL section](https://github.com/StroescuDiana/manual_testing_portofolio/tree/main/Final%20Project#2-sql-section).**

Tools used: JIRA, Zephyr Squad, Postman, MySQL Workbench.

# Functional specifications

The below Story was created in JIRA and describes the functional specifications of the Dependants module, for which the final project is performed upon. 

<img width="1014" alt="2023-06-01_10h38_57" src="https://github.com/StroescuDiana/manual_testing_portofolio/assets/129664856/7ae8f888-8f36-40cd-8ca1-4ebae83526ee">


# 1 Testing section

## 1.1 Test Planning

The Test Plan is designed to describe all details of testing the Add product to cart module from the OpenCart application. 

The plan identifies the items to be tested, the features to be tested, the types of testing to be performed, the personnel responsible for testing, the resources and schedule required to complete testing, and the risks associated with the plan

#### 1.1.1 Roles assigned to the project and persons allocated

* Project manager - Stroescu Diana-Lavinia
* Product owner - Stroescu Diana-Lavinia
* Software developer - Stroescu Diana-Lavinia
* QA Engineer - Stroescu Diana-Lavinia

#### 1.1.2 Entry criteria defined

* functional specifications are defined
* roles needed for the project are allocated
* initial project risks were detected and mitigated

#### 1.1.3 Exit criteria defined

* number of unresolved bugs is insignificant or they have low priority
* all tests have been executed
* all resolved bugs have been re-tested and approved by the QA team
* deadline was reached
* no detected major risk remained un-mitigated
* exploratory regression testing must be performed on the Add product to cart module

#### 1.1.4 Test scope

* __Tests in scope:__ All the features of Add product to cart module which were defined in software requirement specs need to be tested: functional testing, GUI testing and API testing ???
* __Tests not in scope:__ performance testing, integrations of the Add product to cart module with other modules, compatibility testing with multiple browsers

#### 1.1.5 Risks detected

* Project risks: lack of experience of the QA team, short deadline of Zephyr Squad trial, unavailability of test environment
* Product risks: The Add product to cart module does not perform according to the requirements.

#### 1.1.6 Evaluating entry criteria

The entry criterias defined in the Test Planning phase have been achieved and the test process can continue. 

## 1.2 Test Monitoring and Control

Various periodic reports were generated to reflect the current status of the testing process, in case of major problems control measures could be taken.
The following status report was generated after 40% of the test cases were executed, on (de completat cu data):

![image](https://user-images.githubusercontent.com/99291143/163689699-e0295daa-e5dc-4e87-a984-546d9351fbac.png)


## 1.3 Test Analysis

The testing process will be executed based on the above requirements for the Dependents module. The following test conditions were found:
 * Enter data only for mandatory fields and check that the dependant is created/updated
 * Enter data for all available fields and check that the dependant is created/updated
 * Leave mandatory fields empty and check that the dependant cannot be created/updated
 * View dependant details and check they are correct
 * View all dependants in a list
 * Check all validation constraints for the fields

## 1.4 Test Design

Functional test cases were created in Zephyr Squad. Based on the analysis of the specifications, the test design techniques used for generating test cases 
are boundary value analysis, equivalence partitioning and use case testing.

**Test cases:**

![image](https://user-images.githubusercontent.com/99291143/163688901-26234e0a-abfa-4034-93bf-bca37ad2b50c.png)


The test cases with steps can be viewed here: [Dependents_test_cases.pdf](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/Dependents_test_cases.pdf)

For the Dependants API, the following checklist was generated: [API_test_checklist.csv](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/API_test_checklist.csv)


## 1.5 Test Implementation

The following elements are needed to be ready before the test execution phase begins:

* Testing environment is up and running: (de completat)
* Access to the testing environment is given: Username : Admin | Password : admin123
* Cycle summary was created 
* Test cases were added to the cycle summary
* Postman collection with the dependents API methods was created 
* Authorization token was created for accessing the API

## 1.6 Test Execution

* Test cases are executed on the created test Cycle summary: [Dependents_cycle_summary_execution.pdf](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/Dependents_cycle_summary_execution.pdf)
* Bugs have been created based on the failed tests. The complete bug reports can be found here: [Dependents_created_bugs.pdf](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/Dependents_created_bugs.pdf)
    *  Date format is not dd/mm/yyyy
    *  Future "Date of Birth" can be selected from calendar
    *  Only 50 characters are allowed for "Please Specify" field
    *  Only 50 characters are allowed for "Name" field
    *  Relationship "parent" is missing
* API tests are executed based on the checklist. The collection used can be found here: [JSON file with the collection of requests created for the Dependents API](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/OrangeHRM%20API%20-%20Dependents.postman_collection.json)
* Full regression testing is needed after the bugs are fixed

## 1.7 Test Completion

* As the Exit criteria were met and satisfied as mentioned in the appropriate section, this feature is suggested to ‘Go Live’ by the Testing team
* The traceability matrix was generated and can be found here: [Traceability_matrix.csv](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/Traceability_matrix.xlsx)
* Test execution chart was generated, the final report shows that a number (de completat) tests have failed of a total of (de completat) 
* A number of (de completat) test cases were planned for execution and all of them were executed
* A number of (de completat) total bugs were found, from which the priority is: (de completat) is high, (de completat) are medium and (de completat) is low

![image](https://user-images.githubusercontent.com/99291143/163691281-5ccb211d-c101-40ea-bb64-1a4f65f8e1b1.png)


# 2 SQL section

Created a database named '(de completat)' and a table named '(de completat)' with all the columns needed to save data per specifications. Performed different queries inside the sql file: [dependents.sql](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/dependents.sql)

