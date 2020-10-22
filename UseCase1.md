# 1 Use-Case Name
Edit user profile

## 1.1 Brief Description
Edit the information in the user profile which is shown on the user page, such as:
- profile picture
- nickname
- description

# 2 Flow of Events
## 2.1 Basic Flow
- User clicks on "edit" button
- Redirect to edit page
- User edits his data
- User clicks on "save"
- Confirmation Dialog is shown
- Redirect on user page

### 2.1.1 Activity Diagram
![Organization Application Activity Diagram](../Diagrams/UCs/CreateOperationActivityDiagramm.jpg)

### 2.1.2 Mock-up
![Create Operation Form Wireframe](../Pictures/Wireframes/CreateOperation.png)

### 2.1.3 Narrative
```gherkin
Feature: edit user profile

  As a signed in user
  i want to edit my user profile

  Background:
    And I am on the main page

  Scenario: open user page
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "main" page
    When I press the "user" button
    Then I am on the "user" page

  Scenario: edit user page
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "user" page
    When I click the "edit" button
    I get redirected to the "edit" page
    I can upload a new profile picture
    And I can change my nickname
    And I can change my description
    When I press the "save" button
    Then a confirmation Dialog is shown
    Then I am on the "user" page again

  Scenario: enter invalid picture
  If the uploaded picture is not png, jpeg
  Then a error message is shown
  And the process is being canceled
```

## 2.2 Alternative Flows
(n/a)

# 3 Special Requirements
(n/a)

# 4 Preconditions
## 4.1 Login
The user has to be logged in to the system.

# 5 Postconditions
(n/a)

# 6 Extension Points
(n/a)
