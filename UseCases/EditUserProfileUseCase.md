# 1 Use-Case Specification: Edit user profile

## 1.1 Brief Description

Edit the information in the user profile which is shown on the user page, such as:

- profile picture
- username
- description

## 1.2 Mockup

TODO

## 1.3 Screenshot

TODO

# 2 Flow of Events

## 2.1 Basic Flow

- User clicks on "Edit profile" button
- Redirect to "Edit profile" page
- User changes the data
- User clicks on "Save" button
- Confirmation is shown
- Redirect to "Profile" page

### 2.1.1 Activity Diagram

![ActivityDiagram](../Diagrams/Activity%20Diagrams/EditUserProfileActivityDiagram.png)

### 2.1.2 .featureFile

[.feature File EditUserProfile](https://github.com/LorenzSeufert/CeangalMessenger---Code/blob/master/Kotlin-Backend/src/test/resources/cucumber/EditUserProfile.feature)

```Gherkin
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

The user has to be logged in to the application.

# 5 Postconditions

The user data gets changed.

# 6 Function Points

![FP](../Diagrams/FP%20UseCases/EditUserProfileFP.png)

![ComplexityTable](../FunctionPoints/ComplexityAdjustmentTable.png)