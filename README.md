# Reddit - Test Plan

## Revision History

| Date       | Description                        | Author          | Comments                      |
|------------|------------------------------------|-----------------|-------------------------------|
| 02.05.2024 | Test Plan for Reddit Version 2024  | Boier Alexandru | Test plan version 1.0 (initial version) |

## Table of Contents

1. [Introduction](#1-introduction)
   1. [Project Objective](#11-project-objective)
   2. [Functionalities in Scope](#12-functionalities-in-scope)
   3. [Functionalities and Tests Out of Scope](#13-functionalities-and-tests-out-of-scope)
2. [Test Process](#2-test-process)
   1. [Test Planning](#21-test-planning)
   2. [Test Analysis](#22-test-analysis)
   3. [Test Design](#23-test-design)
   4. [Test Implementation](#24-test-implementation)
   5. [Test Execution](#25-test-execution)
   6. [Test Closure](#26-test-closure)
   7. [Test Monitoring and Control](#27-test-monitoring-and-control)
3. [Test Deliverables](#3-test-deliverables)
   1. [Traceability Matrix](#31-traceability-matrix)
   2. [Test Case Results](#32-test-case-results)
   3. [Bugs Report](#33-bugs-report)
4. [Schedule](#4-schedule)

## 1. Introduction

The purpose of this test plan is to outline the strategy, approach, resources, and schedule for testing the Reddit web application. The goal is to ensure the application meets the requirements and performs effectively in terms of functionality, performance, security, and usability.

### 1.1 Project Objective

The project objective of this test plan includes testing all core functionalities of the Reddit web application, including user registration, login, post creation, commenting, voting, and browsing subreddits.

- **Application under test**: [https://www.reddit.com/](https://www.reddit.com/)
- **Application documentation**:
  - [API documentation](https://www.reddit.com/dev/api/)
  - [User guide](https://support.reddithelp.com/hc/en-us/categories/200073949-Getting-Started)

### 1.2 Functionalities in Scope

For this version of the application, the functionalities in the scope of testing are:

- Functional testing of user registration, login, and profile management
- Functional testing of post creation, commenting, and voting
- Functional testing of subreddit creation, subscription, and management
- Performance testing of page load times and response times under various conditions
- Security testing of user authentication, authorization, and data privacy
- Compatibility testing across different web browsers and devices

### 1.3 Functionalities and Tests Out of Scope

- Usability testing
- Testing of Reddit's mobile applications
- Load testing beyond normal usage scenarios

## 2. Test Process

### 2.1 Test Planning

**Roles and responsibilities:**

- **Alexandra Preja** - Test lead - Will monitor the testing process
- **Boier Alexandru** - Senior Tester - Will write the test conditions and test cases for Reddit Web

**Entry criteria:**

- Completion of code development for the functionalities to be tested
- Test environment setup
- Test data preparation

**Exit criteria:**

- All critical and high-severity defects are resolved
- 100% execution of test cases with a pass rate of at least 95%
- All test deliverables are completed and reviewed

**Project risks:**

- The team does not have the proper knowledge and experience for web testing
- Test environment not working
- Short/tight deadlines
- Due to the company changes, we might have leavers
- A high number of defects discovered during testing can extend the testing phase and delay project completion

**Product risks:**

- Validation constraints on some of the fields might be too restrictive
- The application may not function correctly across different web browsers and devices
- The application may not comply with relevant legal and regulatory requirements, leading to potential legal issues
- Potential security vulnerabilities could lead to data breaches or unauthorized access
- The application may not perform well under high user loads, leading to slow response times or crashes

### 2.2 Test Analysis

**Analyzing Business Requirements:**

To ensure that we have all the details necessary for creating the test conditions, we need to thoroughly analyze the business requirements of the Reddit web application. Here’s the approach to follow:

- **Review Business Requirements Document (BRD):**
  - Understand the core functionalities Reddit offers, such as user registration, post creation, commenting, voting, and subreddit management.
  - Identify the key business goals, such as enhancing user engagement, ensuring data security, and providing a seamless user experience.
  
- **Stakeholder Interviews:**
  - Engage with stakeholders (product owners, developers, end-users) to clarify any ambiguities in the requirements.
  - Gather additional insights on critical functionalities and performance expectations.
  
- **Cross-Referencing Design Documents:**
  - Compare business requirements with design documents to ensure alignment between what is required and what is being built.
