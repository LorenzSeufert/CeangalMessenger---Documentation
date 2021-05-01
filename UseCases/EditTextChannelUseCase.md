# 1 Use-Case Specification: Edit text channel

## 1.1 Brief Description

The user edits a created text channel, like the name, members, description.

## 1.2 Mockup

TODO

## 1.3 Screenshot

TODO

# 2 Flow of Events

## 2.1 Basic Flow

- User clicks on "Text channels" button
- Redirect to "Text channels" page
- A list is shown of all text channels
- User selects a text channel
- User clicks on "Edit" button
- User changes data of text channel
- User clicks "Save" button
- User is redirected to the text channel

### 2.1.1 Activity Diagram

![ActivityDiagram](../Diagrams/Activity%20Diagrams/EditTextChannelActivityDiagram.png)

### 2.1.2 .featureFile

TODO

## 2.2 Alternative Flows

(n/a)

# 3 Special Requirements

(n/a)

# 4 Preconditions

- The user has to be logged in to the application.
- The user is member of the text channel.
- The user has admin privileges for the text channel.

# 5 Postconditions

The text channel data changes.

# 6 Function Points

![FP](../Diagrams/FP%20UseCases/EditTextChannelFP.png)

![ComplexityTable](../FunctionPoints/ComplexityAdjustmentTable.png)
