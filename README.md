# Reddit Test Plan

## Revision History

| Date       | Description                  | Author          | Comments                   |
|------------|------------------------------|-----------------|----------------------------|
| 02.05.2024 | Test Plan for Reddit Version 2024 | Boier Alexandru | Test plan version 1.0 (initial version) |

## Table of Contents
1. [Introduction](#introduction)
    1. [Project Objective](#project-objective)
    2. [Functionalities in Scope](#functionalities-in-scope)
    3. [Functionalities and Tests Out of Scope](#functionalities-and-tests-out-of-scope)
2. [Test Process](#test-process)
    1. [Test Planning](#test-planning)
    2. [Test Analysis](#test-analysis)
    3. [Test Design](#test-design)
    4. [Test Implementation](#test-implementation)
    5. [Test Execution](#test-execution)
    6. [Test Closure](#test-closure)
    7. [Test Monitoring and Control](#test-monitoring-and-control)
3. [Test Deliverables](#test-deliverables)
    1. [Traceability Matrix](#traceability-matrix)
    2. [Test Case Results](#test-case-results)
    3. [Bugs Report](#bugs-report)
4. [Schedule](#schedule)

## Introduction

The purpose of this test plan is to outline the strategy, approach, resources, and schedule for testing the Reddit web application. The goal is to ensure the application meets the requirements and performs effectively in terms of functionality, performance, security, and usability.

### Project Objective

The project objective of this test plan includes testing all core functionalities of the Reddit web application, including user registration, login, post creation, commenting, voting, and browsing subreddits.

- **Application under test**: [Reddit](https://www.reddit.com/)
- **Application documentation**: 
  - [API documentation](https://www.reddit.com/dev/api/)
  - [User guide](https://support.reddithelp.com/hc/en-us/categories/200073949-Getting-Started)

### Functionalities in Scope

For this version of the application, the functionalities in the scope of testing are:

- Functional testing of user registration, login, and profile management
- Functional testing of post creation, commenting, and voting
- Functional testing of subreddit creation, subscription, and management
- Performance testing of page load times and response times under various conditions
- Security testing of user authentication, authorization, and data privacy
- Compatibility testing across different web browsers and devices

### Functionalities and Tests Out of Scope

- Usability testing
- Testing of Reddit's mobile applications
- Load testing beyond normal usage scenarios

## Test Process

### Test Planning

#### Roles and Responsibilities

| Role             | Person                | Responsibilities                          |
|------------------|-----------------------|-------------------------------------------|
| Test Lead        | Alexandra Preja       | Monitor the testing process               |
| Senior Tester    | Boier Alexandru       | Write the test conditions and test cases for Reddit Web |

#### Entry Criteria

- Completion of code development for the functionalities to be tested
- Test environment setup
- Test data preparation

#### Exit Criteria

- All critical and high-severity defects are resolved
- 100% execution of test cases with a pass rate of at least 95%
- All test deliverables are completed and reviewed

#### Project Risks

- The team does not have the proper knowledge and experience for web testing
- Test environment not working
- Short/tight deadlines
- Due to company changes, we might have leavers
- A high number of defects discovered during testing can extend the testing phase and delay project completion

#### Product Risks

- Validation constraints on some of the fields might be too restrictive
- The application may not function correctly across different web browsers and devices
- The application may not comply with relevant legal and regulatory requirements, leading to potential legal issues
- Potential security vulnerabilities could lead to data breaches or unauthorized access
- The application may not perform well under high user loads, leading to slow response times or crashes

### Test Analysis

Analyzing Business Requirements

- **Review Business Requirements Document (BRD)**
  - Understand the core functionalities Reddit offers, such as user registration, post creation, commenting, voting, and subreddit management.
  - Identify the key business goals such as enhancing user engagement, ensuring data security, and providing a seamless user experience.
- **Stakeholder Interviews**
  - Engage with stakeholders (product owners, developers, end-users) to clarify any ambiguities in the requirements.
  - Gather additional insights on critical functionalities and performance expectations.
- **Cross-Referencing Design Documents**
  - Compare business requirements with design documents to ensure alignment between what is required and what is being built.
- **User Stories and Use Cases**
  - Break down business requirements into detailed user stories and use cases to understand the practical scenarios users will encounter.
- **Regulatory and Compliance Requirements**
  - Ensure that the application complies with relevant regulations (e.g., GDPR, CCPA) and that these are reflected in the requirements.

### Test Conditions

#### User Registration and Login

1. **Test Condition 1.1**: Verify user registration with valid data.
2. **Test Condition 1.2**: Verify email verification process.
3. **Test Condition 1.3**: Verify user login with valid credentials.
4. **Test Condition 1.4**: Verify password recovery process.

#### Post Creation, Editing, and Deletion

1. **Test Condition 2.1**: Verify creating a post with valid content.
2. **Test Condition 2.2**: Verify editing an existing post.
3. **Test Condition 2.3**: Verify deleting a post.

#### Commenting on Posts

1. **Test Condition 3.1**: Verify adding a comment to a post.
2. **Test Condition 3.2**: Verify editing a comment.
3. **Test Condition 3.3**: Verify deleting a comment.

#### Voting on Posts and Comments

1. **Test Condition 4.1**: Verify upvoting a post.
2. **Test Condition 4.2**: Verify downvoting a post.
3. **Test Condition 4.3**: Verify upvoting a comment.
4. **Test Condition 4.4**: Verify downvoting a comment.

#### Search Functionality

1. **Test Condition 5.1**: Verify searching for posts by keywords.
2. **Test Condition 5.2**: Verify filtering search results by relevance, date, etc.

#### Notifications System

1. **Test Condition 6.1**: Verify receiving notifications for new comments.
2. **Test Condition 6.2**: Verify receiving notifications for upvotes/downvotes.
3. **Test Condition 6.3**: Verify receiving notifications for new posts in subscribed subreddits.

#### Security and Privacy

1. **Test Condition 7.1**: Verify secure login and session management.
2. **Test Condition 7.2**: Verify data encryption during transmission.
3. **Test Condition 7.3**: Verify access control to ensure only authorized users can perform specific actions.

#### Performance

1. **Test Condition 8.1**: Verify page load times under normal user load.
2. **Test Condition 8.2**: Verify application performance under peak user load.
3. **Test Condition 8.3**: Verify response times for search queries and post submissions.

#### Compatibility

1. **Test Condition 11.1**: Verify application functionality on Chrome, Brave, Safari, and Edge.
2. **Test Condition 11.2**: Verify application responsiveness on different screen sizes (desktop, tablet, mobile).

### Test Design

#### Test Scenario 1: User Registration

1. **Test Case 1.1.1: Register with Valid Data**
    - Preconditions: None
    - Steps:
        1. Navigate to the registration page.
        2. Enter valid username, email, and password.
        3. Click "Register."
    - Expected Result: User is registered successfully and redirected to the confirmation page.
    - Pass/Fail Criteria: User is registered and can log in with the provided credentials.

2. **Test Case 1.2.1: Login with Valid Credentials**
    - Preconditions: User is registered.
    - Steps:
        1. Navigate to the login page.
        2. Enter valid username and password.
        3. Click "Login."
    - Expected Result: User is logged in successfully and redirected to the homepage.
    - Pass/Fail Criteria: User can access the homepage and perform authenticated actions.

#### Test Scenario 2: Searching for Posts by Keywords

1. **Test Case 2.1: Search with Common Keyword**
    - Preconditions: User is logged in.
    - Steps:
        1. Navigate to the search bar.
        2. Enter a common keyword.
        3. Press "Enter" or click the search icon.
    - Expected Result: A list of posts containing the keyword is displayed.
    - Pass/Fail Criteria: The search results are relevant and sorted by relevance or date.

2. **Test Case 2.2: Filter Search Results by Relevance**
    - Preconditions: User is logged in and has performed a search.
    - Steps:
        1. Perform a search using any keyword.
        2. Select the "Relevance" filter option.
    - Expected Result: Search results are sorted by relevance.
    - Pass/Fail Criteria: The results are ordered based on how relevant they are to the search query.

#### Test Scenario 3: Creating a Post

1. **Test Case 3.1: Create Post with Valid Data**
    - Preconditions: User is logged in.
    - Steps:
        1. Navigate to the subreddit or home page.
        2. Click "Create Post."
        3. Enter valid title and content.
        4. Click "Submit."
    - Expected Result: Post is created and displayed in the subreddit.
    - Pass/Fail Criteria: Post appears correctly with the entered content.

2. **Test Case 3.2: Delete Existing Post**
    - Preconditions: User is logged in and has an existing post.
    - Steps:
        1. Navigate to the post.
        2. Click "Delete."
        3. Confirm the deletion.
    - Expected Result: Post is deleted and no longer visible.
    - Pass/Fail Criteria: Post is removed from the subreddit.

#### Test Scenario 4: Adding a Comment

1. **Test Case 4.1: Add Comment to Post**
    - Preconditions: User is logged in and viewing a post.
    - Steps:
        1. Navigate to the comments section of the post.
        2. Enter comment content.
        3. Click "Submit."
    - Expected Result: Comment is added and displayed under the post.
    - Pass/Fail Criteria: Comment appears correctly with the entered content.

#### Test Scenario 5: Voting on a Post

1. **Test Case 5.1: Upvote a Post**
    - Preconditions: User is logged in.
    - Steps:
        1. Navigate to the post.
        2. Click "Upvote."
    - Expected Result: Upvote count increases by one.
    - Pass/Fail Criteria: Upvote count is updated correctly.

#### Test Scenario 6: Receive Notification for Reply to User’s Comment

1. **Preconditions**: User is logged in and has commented on a post.
    - Steps:
        1. Another user replies to the user's comment.
    - Expected Result: The user receives a notification about the reply.
    - Pass/Fail Criteria: The notification appears in the user's notification list with correct details about the reply.

### Test Implementation

- Verify if the test environment is up and running
- Access to the test environment is given: valid username and valid password
- Create test suites (Test cycles)
- Prioritize the test cases based on risks and business priority

### Test Execution

- Execute all functional test cases created in the Test Design phase and set the test case status (passed/failed)
- For the test cases that failed, raise defects
- Run the regression pack
- Retest the bugs fixed by the developers to validate that the issues are not reproduced

### Test Closure

- Analyze if the exit criteria were met and the testing process can be closed
- Generate the traceability matrix
- Generate the test completion report

### Test Monitoring and Control

- In this phase, various periodic reports will be generated to reflect the current status of the testing process. In case of major problems, control measures could be taken.

## Test Deliverables

The following test deliverables will be provided by the end of the testing process and sent to the stakeholders to create the basis of informed decision-making:

- Test Plan Document
- Test Cases and Test Scripts
- Defect Reports
- Test Summary Report
- Test Execution Logs

### Traceability Matrix

### Test Case Results

### Bugs Report

1. **Error at replying to other user's comments**
    - **Description**: When a user attempts to reply to another user's comment, the chatbox to write the comment for the other user does not open; therefore, we can’t reply to a comment.
    - **Reproduction steps**:
        1. Open the Reddit website
        2. Login with valid user credentials
        3. Search for the desired post either on the main page or using the search+filters
        4. Open the comments tab with the "chatbox" icon below the post
        5. Look for the desired comment
        6. Click on the "chatbox" icon below the comment to reply
        7. Write the desired comment in the newly opened field and then click on the "comment" button
    - **Expected Result**: The reply should be posted successfully and appear under the original comment.
    - **Actual Result**: An error message is displayed, and the reply is not posted. The error message reads: "An error occurred while posting your reply. Please try again later."

2. **Error at changing notification settings**
    - **Description**: Users encounter an error when attempting to change their notification settings. The changes are not saved and an error message is displayed.
    - **Reproduction steps**:
        1. Open the Reddit website
        2. Login with valid user credentials
        3. Click on the “bell” icon at the top right of the screen, then on “view settings”
        4. From the notifications tab, tick the desired settings that you wish to have enabled or disabled
        5. Click the "Save" button.
    - **Expected Result**: The user can customize their notification settings
    - **Obtained Result**: The user can’t change any settings because all of them are greyed out

## Schedule

The testing process will take place over a period of 1 week and will involve all the activities defined in the previous section. All resources will be adapted accordingly in case new testing resources are detected as necessary.
