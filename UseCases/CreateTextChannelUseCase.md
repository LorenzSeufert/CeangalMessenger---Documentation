# 1 Use-Case Specification: Create text channel

## 1.1 Brief Description

Every user can create a text channel with multiple friends

- The creator has to enter a name for the text channel
- The creator can add a description to the text channel
- The creator has to add the friends to the text channel

## 1.2 Mockup

TODO

## 1.3 Screenshot

TODO

# 2 Flow of Events

## 2.1 Basic Flow

- User clicks on "Text channels" button
- Redirect to "Text channels" page
- User clicks on "Create text channel" button
- Redirect to "create text channel" page
- User fills out data
- User clicks on "Save" button
- Confirmation Dialog is shown
- Redirect to "Text channels" page

### 2.1.1 Activity Diagram

![ActivityDiagram](../Diagrams/Activity%20Diagrams/CreateTextChannelDiagram.png)

### 2.1.2 .featureFile

[.feature File CreateTextChannel](https://github.com/LorenzSeufert/CeangalMessenger---Code/blob/master/Kotlin-Backend/src/test/resources/cucumber/CreateTextChannel.feature)

```Gherkin
Feature: CreateTextChannel
  AS a signed in user
  I want to create a text channel


  Scenario: Click 'Create text channel' button
    Given I am signed in with username 'USER' and password 'PASSWORD'
    And I am on the "main" page
    When I press the "Create text channel" button
    Then I am on the "Create text channel" page

  Scenario: Fill out data
    Given I am on the "Create text channel" page
    Then I have to fill out the 'name' field
    And I can fill out the 'description' field
    When I press the "Save" button
    Then a confirmation Dialog is shown
    Then I am on the "Text channel" page
```

## 2.2 Alternative Flows

(n/a)

# 3 Special Requirements

The creator has to be friends with the members of the text channel to add them.

# 4 Preconditions

The user has to be logged in to the application.

# 5 Postconditions

The members are added to the text channel.

# 6 Function Points

![FP](../Diagrams/FP%20UseCases/CreateTextChannelFP.png)

![ComplexityTable](../FunctionPoints/ComplexityAdjustmentTable.png)
