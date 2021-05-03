# Test plan

- [Test plan](#test-plan)
    - [1. Introduction](#1-introduction)
        - [1.1 Purpose](#11-purpose)
        - [1.2 Scope](#12-scope)
        - [1.3 Intended Audience](#13-intended-audience)
        - [1.4 Document Terminology and Acronyms](#14-document-terminology-and-acronyms)
        - [1.5  References](#15--references)
        - [1.6 Document Structure](#16-document-structure)
    - [2. Evaluation Mission and Test Motivation](#2-evaluation-mission-and-test-motivation)
        - [2.1 Background](#21-background)
        - [2.2 Evaluation Mission](#22-evaluation-mission)
        - [2.3 Test Motivators](#23-test-motivators)
    - [3. Target Test Items](#3-target-test-items)
    - [4. Outline of Planned Tests](#4-outline-of-planned-tests)
        - [4.1 Outline of Test Inclusions](#41-outline-of-test-inclusions)
        - [4.2 Outline of Other Candidates for Potential Inclusion](#42-outline-of-other-candidates-for-potential-inclusion)
        - [4.3 Outline of Test Exclusions](#43-outline-of-test-exclusions)
    - [5. Test Approach](#5-test-approach)
        - [5.1 Testing Techniques and Types](#51-testing-techniques-and-types)
            - [5.1.1 Unit Testing](#511-unit-testing)
            - [5.1.2 Functional Testing](#512-functional-testing)
            - [5.1.3 API Testing](#513-api-testing)
    - [6. Entry and Exit Criteria](#6-entry-and-exit-criteria)
        - [6.1 Test Plan](#61-test-plan)
            - [6.1.1 Test Plan Entry Criteria](#611-test-plan-entry-criteria)
            - [6.1.2 Test Plan Exit Criteria](#612-test-plan-exit-criteria)
    - [7. Deliverables](#7-deliverables)
        - [7.1 Test Evaluation Summaries](#71-test-evaluation-summaries)
        - [7.2 Reporting on Test Coverage](#72-reporting-on-test-coverage)
        - [7.3 Perceived Quality Reports](#73-perceived-quality-reports)
        - [7.4 Incident Logs and Change Requests](#74-incident-logs-and-change-requests)
        - [7.5 Smoke Test Suite and Supporting Test Scripts](#75-smoke-test-suite-and-supporting-test-scripts)
    - [8. Testing Workflow](#8-testing-workflow)
    - [9. Environmental Needs](#9-environmental-needs)
        - [9.1 Base System Hardware](#91-base-system-hardware)
        - [9.2 Base Software Elements in the Test Environment](#92-base-software-elements-in-the-test-environment)
        - [9.3 Productivity and Support Tools](#93-productivity-and-support-tools)
    - [10. Responsibilities, Staffing, and Training Needs](#10-responsibilities-staffing-and-training-needs)
        - [10.1 People and Roles](#101-people-and-roles)
        - [10.2 Staffing and Training Needs](#102-staffing-and-training-needs)
    - [11. Iteration Milestones](#11-iteration-milestones)
    - [12. Risks, Dependencies, Assumptions, and Constraints](#12-risks-dependencies-assumptions-and-constraints)
    - [13. Management Process and Procedures](#13-management-process-and-procedures)

## 1. Introduction

### 1.1 Purpose

The purpose of the Iteration Test Plan is to gather all of the information necessary to plan and control the test effort
for a given iteration. It describes the approach to testing the software. This Test Plan for Ceangal Messenger supports
the following objectives:

- Identifies the items that should be targeted by the tests.
- Identifies the motivation for and ideas behind the test areas to be covered.
- Outlines the testing approach that will be used.
- Identifies the required resources and provides an estimate of the test efforts.

### 1.2 Scope

This test plan will cover tests assuring the functionality of the application's front end, back end and the
communication between the two. This document shows the following types of testing:

- Unit Testing
- Functional Testing
- API Testing

Not covered are any tests related to performance and scale or usability.

### 1.3 Intended Audience

This test plan is written primarily for internal documentation reasons. It is meant to provide orientation to the
developers to work from and as a documentation to measure the fullfillment of quality requirements against.

### 1.4 Document Terminology and Acronyms

| Abbr | Abbreviation                        |
|------|-------------------------------------|
| API  | Application Programmable Interface  |
| CI   | Continuous Integration              |
| CD   | Continuous Delivery/Deployment      |
| N/A  | not applicable                      |
| SRS  | Software Requirements Specification |
| TBD  | to be determined                    |
| UI   | User Interface                      |
| VC   | Version Control                     |
| TDD  | Test Driven Development             |

### 1.5  References

| Title                                                                          |Publishing organization    |
| -------------------------------------------------------------------------------|---------------------------|
| [Blog](https://ceangalmessenger.wordpress.com/)                                | Ceangal Team              |
| [GitHub Repository](https://github.com/LorenzSeufert/CeangalMessenger---Code)  | Ceangal Team              |
| [UC1 Add friend](./UseCases/AddFriendUseCase.md)                               | Ceangal Team              |
| [UC2 Create text channel](./UseCases/CreateTextChannelUseCase.md)              | Ceangal Team              |
| [UC3 Create user profile](./UseCases/CreateUserProfileUseCase.md)              | Ceangal Team              |
| [UC4 Delete account](UseCases/DeleteAccountUseCase.md)                         | Ceangal Team              |
| [UC5 Edit text channel](./UseCases/EditTextChannelUseCase.md)                  | Ceangal Team              |
| [UC6 Edit user profile](./UseCases/EditUserProfileUseCase.md)                  | Ceangal Team              |
| [UC7 Send private message](./UseCases/SendFriendsPrivateTextMessageUseCase.md) | Ceangal Team              |
| [UC8 Show friends](./UseCases/ShowFriendsUseCase.md)                           | Ceangal Team              |
| [Test Plan](./TestPlan.md)                                                     | Ceangal Team              |
| [SRS](./Software_Requirements_Specification.md)                                | Ceangal Team              |
| [SAD](./SAD.md)                                                                | Ceangal Team              |

### 1.6 Document Structure

n/a

## 2. Evaluation Mission and Test Motivation

### 2.1 Background

Testing serves to ensure that the written code does what it is intended to do. It also prevents future code changes to
break existing functionality unnoticed. In the context of integration it can also prevent broken software states to be
merged into secured VC branches

### 2.2 Evaluation Mission

Testing is a crucial phase in the development cycle. It is necessary in order to fix technical bugs and important
functional problems. With TDD we define the test first and can fix bugs before they even occur.

### 2.3 Test Motivators

The tests are done to ensure quality and mitigate risks and fulfill functional requirements. Their purpose is to provide
stability for our application.

## 3. Target Test Items

- Electron frontend
- Server backend (API)

## 4. Outline of Planned Tests

### 4.1 Outline of Test Inclusions

*Frontend: Electron Desktop Client*:

- Unit testing

*Backend: Spring Boot Application*:

- Unit testing
- Functional testing
- Api testing

The tests themself will not be tested and will not account into code coverage.

### 4.2 Outline of Other Candidates for Potential Inclusion

n/a

### 4.3 Outline of Test Exclusions

Because of time and resource constraints we will not do:

- Stress test
- Load/performance tests
- Usability tests
- UI tests
- any further tests

## 5. Test Approach

### 5.1 Testing Techniques and Types

#### 5.1.1 Unit Testing

Unit testing ensures, that the tested sourcecode works as expected. Therefore small parts like methods of the sourcecode
are tested.

|                       | Description                                                               |
|-----------------------|---------------------------------------------------------------------------|
|Technique Objective    | Ensure that the implemented code works as expected                        |
|Technique              | Implement test methods using JUnit and MochaJS                            |
|Oracles                | Test execution logs results to the command line in IDE and GitHub Actions |
|Required Tools         | JUnit 5 and MochaJS Dependencies in Frontend and Backend                  |
|Success Criteria       | All tests pass in IDE and GitHub Actions                                  |
|Special Considerations | -                                                                         |

#### 5.1.2 Functional Testing

Functional testing is to develop test cases to test the behavior of software's functionality.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Ensure that the application behaves correct                          |
|Technique              | Writing Gherkin `.feature` files with clearly defined steps and the expected result. Written in simple english.|
|Oracles                | Test execution logs results to the command line in IDE and GitHub Actions |
|Required Tools         | Dependencies of Cucumber and JUnit to execute tests                  |
|Success Criteria       | All cucumber tests pass.
|Special Considerations | - |

#### 5.1.3 API Testing

Api Testing is to test the endpoints of the application. The main goal of Api testing is to ensure, that the provided
API of the Backend behave as expected.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Test the endpoints with JUnit (MockMVC)                                 |
|Technique              | For every important endpoint of the API an test exists  |            
|Oracles                | Test execution logs results to the command line in IDE and GitHub Actions |
|Required Tools         | JUnit                                    |
|Success Criteria       | All tests of the endpoints pass.                               |
|Special Considerations | -                                                                    |

## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria

n/a

#### 6.1.2 Test Plan Exit Criteria

n/a

## 7. Deliverables

## 7.1 Test Evaluation Summaries

TODO

## 7.2 Reporting on Test Coverage

TODO

## 7.3 Perceived Quality Reports

TODO

## 7.4 Incident Logs and Change Requests

TODO

## 7.5 Smoke Test Suite and Supporting Test Scripts

TODO

## 8. Testing Workflow

1) Local testing in the IDE
2) Commit and Push triggers build and test exection in the CI/CD Pipeline
3) Each PR triggers the pipeline (build and test)

## 9. Environmental Needs

### 9.1 Base System Hardware

The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource              | Quantity | Name and Type                |
|-----------------------|:--------:|------------------------------|
| CI/CD server          |    1     | GitHub Actions               |
| local test machine    |    1     | computer (Ceangal Team       |

### 9.2 Base Software Elements in the Test Environment

The following base software elements are required in the test environment for this Test Plan.

| Software Element Name |  Type and Other Notes                        |
|-----------------------|----------------------------------------------|
| IntelliJ              | Test Runner / IDE                            |
| JUnit 5               | Unit testing backend / API testing           |
| Cucumber              | Functional testing                           |
| MochaJS               | Unit testing frontend                        |

### 9.3 Productivity and Support Tools

The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name                                      |
|-----------------------|------------------------------------------------------|
| Repository            | [GitHub](http://github.com/)                         |
| CI/CD Service         | [GitHub Actions](https://github.com/features/actions)|

## 10. Responsibilities, Staffing, and Training Needs

### 10.1 People and Roles

| Role                      | Person Assigned             |  Specific Responsibilities or Comments |
|---------------------------|:---------------------------:|----------------------------------------|
| Test Manager              | Fabian                      | Provides management oversight. |
| Test Designer             | Fabian,Lennart,David,Lorenz | Defines the technical approach to the implementation of the test effort. |
| Test System Administrator | Fabian,Lennart              | Ensures test environment and assets are managed and maintained. |

### 10.2 Staffing and Training Needs

n/a

## 11. Iteration Milestones

We want to keep over 25% code coverage.

## 12. Risks, Dependencies, Assumptions, and Constraints

TODO

## 13. Management Process and Procedures

n/a
