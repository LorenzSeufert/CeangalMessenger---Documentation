# 1 Use-Case Name
Delete Account

## 1.1 Brief Description
Delete the user account completely, so the database entry gets removed.

# 2 Flow of Events
## 2.1 Basic Flow
- User clicks on "edit" button
- Redirect to edit page
- User clicks on button "delete Account"
- A formula opens with a field for username and password
- User has to enter username and password and press "delete Account"
- Dialog with text "Do you really want to delete your account?" and options "continue" and "cancel" is shown
- User clicks on "continue"
- Account gets deleted
- User will be directed to the log in screen with the message "successfully deleted account"

### 2.1.1 Activity Diagram
![Organization Application Activity Diagram](../Diagrams/Activity%20Diagrams/EditUserProfileActivityDiagram.png)

### 2.1.2 Mock-up


### 2.1.3 Narrative
[Current feature file](https://github.com/LorenzSeufert/CeangalMessenger---Code/blob/master/src/test/resources/cucumber/EditUserProfile.feature)
```gherkin
Feature: EditUserProfile
  AS a signed in user
  I want to edit my user profile

  Scenario Outline: Edit profile
    Given The user is logged in
    Given User is on the profile page
    When I click the button 'Edit profile'
    Then Redirect to the 'edit' page
    Then I can change my description
    And I can change my nickname
    When I upload a picture of <format>
    And I click the button 'Update profile'
    Then <status>-Popup with <message>

    Examples:
      | format | status | message         |
      | png    | OK     | Profile updated |
      | jpeg   | OK     | Profile updated |
      | gif    | ERROR  | Invalid format  |

  Scenario: Open user page
    Given I am signed in with username 'USER' and password 'PASSWORD'
    And I am on the "main" page
    When I press the "user" button
    Then I get on the "user" page
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
