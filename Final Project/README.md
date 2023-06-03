# Practice Project Manual Testing

The scope of the final project for ITF Manual Testing Course is to use all gained knowledge through the course and apply them in practice, using a live application. 

Application under test: https://demo.opencart.com/

API Documentation: https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md

**The final project will be split into 2 sections: [Testing section](https://github.com/StroescuDiana/manual_testing_portofolio/tree/main/Final%20Project#1-testing-section) and [SQL section](https://github.com/StroescuDiana/manual_testing_portofolio/tree/main/Final%20Project#2-sql-section).**

Tools used: JIRA, Zephyr Squad, Postman, MySQL Workbench.

# Functional specifications

The below Story was created in JIRA and describes the functional specifications of the Add product to cart module, for which the final project is performed upon. 

<img width="1014" alt="2023-06-01_10h38_57" src="https://github.com/StroescuDiana/manual_testing_portofolio/assets/129664856/7ae8f888-8f36-40cd-8ca1-4ebae83526ee">


# 1 Testing section

## 1.1 Test Planning

The Test Plan is designed to describe all details of testing the Add product to cart module from the OpenCart application. 

The plan identifies the items to be tested, the features to be tested, the types of testing to be performed, the personnel responsible for testing, the resources and schedule required to complete testing, and the risks associated with the plan.

#### 1.1.1 Roles assigned to the project and persons allocated

* Project manager - Sylvia Gould
* Product owner - Oliwia Romero
* Software developer - Cory John
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

* __Tests in scope:__ All the features of Add product to cart module which were defined in software requirement specs need to be tested: functional testing, GUI testing and API testing.
* __Tests not in scope:__ performance testing, integrations of the Add product to cart module with other modules, compatibility testing with multiple browsers.

#### 1.1.5 Risks detected

* Project risks: Lack of experience of the QA team, short deadline of Zephyr Squad trial, unavailability of test environment.
* Product risks: The Add product to cart module does not perform according to the requirements.

#### 1.1.6 Evaluating entry criteria

The entry criterias defined in the Test Planning phase have been achieved and the test process can continue. 

## 1.2 Test Monitoring and Control

Various periodic reports were generated to reflect the current status of the testing process, in case of major problems control measures could be taken.
The following status report was generated after 60% of the test cases were executed, on 2nd of June:

<img width="810" alt="2023-06-02_21h54_57" src="https://github.com/StroescuDiana/manual_testing_portofolio/assets/129664856/fd3ba422-0c05-4a6e-9888-0de20b86f195">


## 1.3 Test Analysis

The testing process will be executed based on the above requirements for the Add to cart module. The following test conditions were found:
 * Any product available on the website can be added to the cart.
 * When a user opens the website, the cart feature is easy to find and use.
 * In the cart page, each product added has the name and price displayed.
 * The cart can store multiple products.
 * With each product added, the cart is able to calculate the total price.

## 1.4 Test Design

Functional test cases were created in Zephyr Squad. Based on the analysis of the specifications, the test design techniques used for generating test cases 
are boundary value analysis, equivalence partitioning and use case testing.

**Test cases:**

<img width="803" alt="2023-06-02_22h15_40" src="https://github.com/StroescuDiana/manual_testing_portofolio/assets/129664856/fb2c83a6-2f78-44b5-bbd5-67ad9ff911c8">


The test cases with steps can be viewed here: [Functional test cases](https://github.com/StroescuDiana/manual_testing_portofolio/assets/129664856/8620641c-a76e-447e-80e1-2473dbee65f1)


For the Simple Books API, the following checklist was generated: 


| GET /orders/:orderId                                              | PATCH /orders/:orderId                                                      | DELETE /orders/:orderId                        |
| ----------------------------------------------------------------  | --------------------------------------------------------------------------  | -------------------------------------------- |
| Verify if an order is returned                                    | Verify if customerName can be updated                                       | Verify if an order can be deleted             |
| Verify if an invalid orderId gives error code                     | Verify if customerName can be updated with numbers and special characters   | Verify if an invalid orderId can be deleted    |
| Verify if an invalid orderId gives incorrect orderId message      | Verify if customerName can be updated by leaving it empty                   | Verify if an empty orderId can be deleted     |



## 1.5 Test Implementation

The following elements are needed to be ready before the test execution phase begins:

* Testing environment is up and running: https://demo.opencart.com/
* Cycle summary was created.
* Test cases were added to the cycle summary.
* Postman collection with the API methods was created. 
* Authorization token was created for accessing the API.

## 1.6 Test Execution

* Test cases are executed on the created test Cycle summary: [Functional test cases](https://github.com/StroescuDiana/manual_testing_portofolio/assets/129664856/8620641c-a76e-447e-80e1-2473dbee65f1)
* Bugs have been created based on the failed tests. The complete bug reports can be found here: [Bug reports](https://github.com/StroescuDiana/manual_testing_portofolio/assets/129664856/6163221c-fb54-4a03-9439-5c36aec7a28a)

    *  Products are not aligned correctly on the homepage's featured products.
    *  User is able to register an account with non-letter characters(numbers, special characters) in the name field.
    *  Unable to add product from homepage to shopping cart.
    *  In the register form the error messages for each field does not appear when criterias aren't met.
    *  User cannot search the item in the search box.
* API tests are executed based on the checklist. The collection used can be found here: [JSON file with the collection of requests created for the Simple Books API](https://github.com/StroescuDiana/manual_testing_portofolio/blob/main/Final%20Project/Simple%20Books%20API.postman_collection.json)
* Full regression testing is needed after the bugs are fixed.

## 1.7 Test Completion

* As the Exit criteria were met and satisfied as mentioned in the appropriate section, this feature is suggested to ‘Go Live’ by the Testing team.
* The traceability matrix was generated and can be found here: [Traceability_matrix.csv](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/Traceability_matrix.xlsx)
* Test execution chart was generated, the final report shows that a number of 11 tests have failed of a total of 19. 
* A number of 19 test cases were planned for execution and all of them were executed.
* A number of 11 bugs were found, from which the priority is: 2 are highest, 3 are high, 5 are medium and 1 is low.

![image](https://user-images.githubusercontent.com/99291143/163691281-5ccb211d-c101-40ea-bb64-1a4f65f8e1b1.png)


# 2 SQL section

Created a database named '(de completat)' and a table named '(de completat)' with all the columns needed to save data per specifications. Performed different queries inside the sql file: [dependents.sql](https://github.com/julai215/itf_final_project_example_and_portofolio/blob/main/Final%20Project/dependents.sql)

