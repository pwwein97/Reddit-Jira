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
  ### User Stories and Use Cases

- **User Stories and Use Cases:**
  - Break down business requirements into detailed user stories and use cases. This helps in understanding the practical scenarios users will encounter.
- **Regulatory and Compliance Requirements:**
  - Ensure that the application complies with relevant regulations (e.g., GDPR, CCPA) and that these are reflected in the requirements.

### Test Conditions

#### Authentication and Authorization

- **Test Condition 1.1:** Verify user registration with valid data.
- **Test Condition 1.2:** Verify user authentication with valid credentials.
- **Test Condition 1.3:** Verify password recovery process.

#### Browsing and Viewing Content

- **Test Condition 2.1:** Verify homepage accessibility with infinite scroll.
- **Test Condition 2.2:** Verify filtering search results by relevance, date, etc.
- **Test Condition 2.3:** Verify display of comments inside a post.

#### Creating and Managing Posts

- **Test Condition 3.1:** Verify creating a post with valid content.
- **Test Condition 3.2:** Verify editing an existing post.
- **Test Condition 3.3:** Verify deleting a post.

#### Comments and Votes

- **Test Condition 4.1:** Verify adding a comment to a post.
- **Test Condition 4.2:** Verify if a user can reply to another user’s comment.
- **Test Condition 4.3:** Verify voting on comments.
- **Test Condition 4.4:** Verify filtering and sorting comments.
- **Test Condition 4.5:** Verify deleting a comment.

#### Searching for Posts by Keyword and Filtering

- **Test Condition 5.1:** Verify if users can search results by common keyword.
- **Test Condition 5.2:** Verify if users can combine search with filtering.

#### Notifications System

- **Test Condition 6.1:** Verify receiving notifications for user activity.
- **Test Condition 6.2:** Verify receiving notifications for direct messages and mentions.
- **Test Condition 6.3:** Verify being able to change notification settings and preferences.

### 2.3 Test Design

#### Test Scenario 1: User Registration and Login

- **Test Case 1.1: Register with Valid Data**
  - **Preconditions:**
    - Working internet connection.
    - Access to the Reddit webpage.
  - **Steps:**
    1. Navigate to the registration page.
    2. Enter valid username, email, and password.
    3. Click "Register."
  - **Expected Result:** User is registered successfully and redirected to the confirmation page.
  - **Pass/Fail Criteria:** User is registered and can log in with the provided credentials.

- **Test Case 1.2: Login with Valid Credentials**
  - **Preconditions:** User is registered.
  - **Steps:**
    1. Navigate to the login page.
    2. Enter valid username and password.
    3. Click "Login."
  - **Expected Result:** User is logged in successfully and redirected to the homepage.
  - **Pass/Fail Criteria:** User can access the homepage and perform authenticated actions.

- **Test Case 1.3: Password Reset Functionality**
  - **Preconditions:** User has a registered account.
  - **Steps:**
    1. Open Reddit website and initiate password reset.
    2. Check registered e-mail address for password reset request.
    3. Enter new password.
    4. Submit new password.
    5. Log in with new password.
  - **Expected Result:** User is able to log in successfully with the new password.
  - **Pass/Fail Criteria:** The user is able to log in with the new password without encountering any error messages or login failures.

#### Test Scenario 2: User Navigation and Content Accessibility

- **Test Case 2.1: Homepage Accessibility with Infinite Scroll**
  - **Preconditions:** User is logged into the application and is on the homepage.
  - **Steps:**
    1. Scroll down the homepage continuously to trigger the infinite scroll.
    2. Monitor the behavior as new content loads automatically without user interaction.
    3. Observe the loading indicator (the Reddit icon pulsing) to ensure it appears and updates appropriately.
  - **Expected Result:** New content loads dynamically and seamlessly as the user scrolls down the homepage.
  - **Pass/Fail Criteria:** Pass if the navigation is smooth, and content loads correctly.

- **Test Case 2.2: Sorting and Filtering Content within Subreddits**
  - **Preconditions:** User is logged into their Reddit account.
  - **Steps:**
    1. Select the sorting option (e.g., "Hot", "New", "Top") from the sorting dropdown.
    2. Select the filtering option (e.g., "today", "this week", "this month") from the filtering dropdown.
    3. Observe the content displayed according to the selected sorting and filtering options.
  - **Expected Result:** The content should be sorted and filtered correctly according to the selected options. The sorting and filtering actions should be responsive and accurate.
  - **Pass/Fail Criteria:** Pass if the content is displayed correctly according to the selected sorting and filtering options. Fail if the content is not displayed correctly or if there are delays/errors.

- **Test Case 2.3: Display of Comments on a Post**
  - **Preconditions:**
    - User is logged into the Reddit web.
    - User is viewing a post with comments.
  - **Steps:**
    1. Make sure you are logged in.
    2. Navigate to a post with comments.
    3. Observe the display of comments.
  - **Expected Result:** Comments should be displayed correctly.
  - **Pass/Fail Criteria:** Pass if comments are displayed correctly.

#### Test Scenario 3: Creating and Managing Posts

- **Test Case 3.1: Creating a New Post**
  - **Preconditions:** User is logged in.
  - **Steps:**
    1. Navigate to the subreddit or home page.
    2. Click "Create Post."
    3. Enter valid title and content.
    4. Click "Submit."
  - **Expected Result:** Post is created and displayed in the subreddit.
  - **Pass/Fail Criteria:** Post appears correctly with the entered content.
 - **Test Case 3.2: Edit an Existing Post**
  - **Preconditions:** User is logged in and has a post created.
  - **Steps:**
    1. Make sure you are logged in.
    2. Navigate to user profile.
    3. Select a post to edit.
    4. Modify post content.
    5. Save changes.
  - **Expected Result:** Changes to the post are saved successfully.
  - **Pass/Fail Criteria:** The changes are saved successfully, and the post updates with the new content.

- **Test Case 3.3: Delete Existing Post**
  - **Preconditions:** 
    1. User is logged in.
    2. User has an existing post.
  - **Steps:**
    1. Navigate to the post.
    2. Click "Delete."
    3. Confirm the deletion.
  - **Expected Result:** Post is deleted and no longer visible.
  - **Pass/Fail Criteria:** Post is removed from the subreddit.

### Test Scenario 4: Comments and Votes

- **Test Case 4.1: Add Comment to a Post**
  - **Preconditions:** User is logged in and viewing a post.
  - **Steps:**
    1. Navigate to the comments section of the post.
    2. Enter comment content.
    3. Click "Submit."
  - **Expected Result:** Comment is added and displayed under the post.
  - **Pass/Fail Criteria:** Comment appears correctly with the entered content.

- **Test Case 4.2: Vote on a Comment**
  - **Preconditions:** User is logged into their Reddit account. User is viewing a post with comments.
  - **Steps:**
    1. Navigate to the comments section of the post.
    2. Identify the comment on which you want to vote.
    3. Click on the upvote or downvote arrow next to the comment.
  - **Expected Result:** The vote count for the comment increases (for upvote) or decreases (for downvote) by one.
  - **Pass/Fail Criteria:** The vote count for the comment accurately reflects the user's action.

- **Test Case 4.3: Reply to an Existing Comment on Reddit**
  - **Preconditions:** User is logged into their Reddit account. User is viewing a post with comments.
  - **Steps:**
    1. Navigate to the comments section of the post.
    2. Identify the comment to which you want to reply.
    3. Click on the "Reply" button.
    4. Enter the reply content and click "Submit."
  - **Expected Result:** The reply is successfully posted and displayed directly beneath the comment.
  - **Pass/Fail Criteria:** The reply is successfully posted and displayed directly beneath the comment.

- **Test Case 4.4: Filtering and Sorting Comments**
  - **Preconditions:** User is logged into their Reddit account. User is viewing a post with multiple comments.
  - **Steps:**
    1. Navigate to the comments section of the post.
    2. Locate the filter options next to "Sort by".
    3. Select a filter criterion such as: Best, Top, New, etc.
  - **Expected Result:** Comments are filtered based on the selected criterion.
  - **Pass/Fail Criteria:** Comments are displayed in the order specified by the selected filter.

- **Test Case 4.5: Deleting a Comment**
  - **Preconditions:** User is logged into their Reddit account. User has previously posted a comment.
  - **Steps:**
    1. Navigate to the post where the comment to be deleted is located.
    2. Locate the comment that the user wants to delete.
    3. Find the "Delete" option or link associated with the comment.
    4. Confirm the deletion action by clicking "Delete" or "Confirm" in the prompt.
  - **Expected Result:** The comment is successfully deleted from the post and no longer visible to other users.
  - **Pass/Fail Criteria:** The comment is successfully deleted from the post and no longer visible to other users.

### Test Scenario 5: Searching for Posts by Keywords and Filtering

- **Test Case 5.1: Search with Common Keyword**
  - **Preconditions:** User is logged in.
  - **Steps:**
    1. Navigate to the search bar.
    2. Enter a common keyword.
    3. Press "Enter" or click the search icon.
  - **Expected Result:** A list of posts containing the keyword is displayed.
  - **Pass/Fail Criteria:** The search results are relevant and sorted by relevance or date.

- **Test Case 5.2: Combination of Search and Filtering**
  - **Preconditions:** User is logged in and has performed a search.
  - **Steps:**
    1. Make sure you are logged in.
    2. Use the search bar.
    3. Apply a filter (from relevance/All time).
  - **Expected Result:** The filtered search results are relevant and adhere to the selected filters.
  - **Pass/Fail Criteria:** The search results are accurate and relevant to the entered query.

### Test Scenario 6: Notifications and Content of Interest

- **Test Case 6.1: Notifications for Comment Replies and Mentions**
  - **Preconditions:** User is logged in and has commented on a post.
  - **Steps:**
    1. Another user replies to the user's comment or mentions them.
  - **Expected Result:** The notification appears in the user's notification list (top right bell icon) with correct details about the reply.
  - **Pass/Fail Criteria:** The user receives a notification about the reply/mention on a post.

- **Test Case 6.2: Notifications for Direct Messages and Mentions**
  - **Preconditions:** User is logged in. User has received a message from another user.
  - **Steps:**
    1. Navigate to the top right of the screen at the "open chat" icon.
    2. The user has a number on top of the icon displaying a new message.
  - **Expected Result:** The user receives a notification about direct messages.
  - **Pass/Fail Criteria:** The notification appears at the top right of the screen on top of the "open chat" icon.
    - **Test Case 6.3: Receiving Notifications Based on Preferences**
  - **Preconditions:** User has customized their notification preferences and enabled notifications.
  - **Steps:**
    1. User must be logged into their Reddit account.
    2. Click on the bell at the top right.
    3. Click on "View Settings."
    4. Choose the desired settings.
  - **Expected Result:** Notifications should be received according to the user's customized preferences.
  - **Pass/Fail Criteria:** Notifications are received correctly as per the preferences.

## 2.4 Test Implementation
- Verify if the test environment is up and running.
- Access to the test environment is given: valid username and valid password.
- Create test suites (Test cycles).
- Prioritize the test cases based on risks and business priority.

## 2.5 Test Execution
- All functional test cases created in the Test Design phase are executed, and we set the test case status (passed/failed).
- For the test cases that failed, we will raise defects.
- Run the regression pack.
- Retesting for the bugs that are fixed by the developers to validate that the issues are not reproduced.

## 2.6 Test Closure
- Analyze if the exit criteria were met and the testing process can be closed.
- Generate the traceability matrix.
- Generate the test completion report.

## 2.7 Test Monitoring and Control
In this phase, various periodic reports will be generated to reflect the current status of the testing process. In case of major problems, control measures could be taken.

## 3. Test Deliverables

The following test deliverables will be provided by the end of the testing process and sent to the stakeholders to create the basis of informed decision:

- Test Plan Document
- Test Cases and Test Scripts
- Defect Reports
- Test Summary Report
- Test Execution Logs

## 3.1 Traceability matrix
![image](https://github.com/pwwein97/Reddit-Jira/assets/164913359/f1e79fe6-640c-43db-a7df-51cb9eef84b0)

## 3.2 Test case results
![image](https://github.com/pwwein97/Reddit-Jira/assets/164913359/e28bf142-ff12-41dc-9977-040af097b810)
![image](https://github.com/pwwein97/Reddit-Jira/assets/164913359/31a52f2c-46f6-4f08-8146-cb7ffb18eb86)



