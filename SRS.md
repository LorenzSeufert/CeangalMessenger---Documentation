# littleBeasts - Software Requirements Specification

## Table of Contents

-   [Flashcard Community - Software Requirements Specification](#flashcard-community---software-requirements-specification)

    -   [Table of Contents](#table-of-contents)

    -   [1. Introduction](#1-introduction)

        -   [1.1 Purpose](#11-purpose)
        -   [1.2 Scope](#12-scope)
        -   [1.3 Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
        -   [1.4 References](#14-references)
        -   [1.5 Overview](#15-overview)

    -   [2. Overall Description](#2-overall-description)

        -   [2.1 Vision](#21-vision)

    -   [2.2 Product perspective](#22-product-perspective)

        -   [2.3 User characteristics](#23-user-characteristics)
        -   [2.4 Dependencies](#24-dependencies)

    -   [3. Specific Requirements](#3-specific-requirements)

        -   [3.1 Functionality � Data Backend](#31-functionality--data-backend)

            -   [3.1.1 Read data given over API endpoints](#311-read-data-given-over-api-endpoints)
            -   [3.1.2 Parse data](#312-parse-data)
            -   [3.1.3 Provide data](#313-provide-data)

        -   [3.2 Functionality � User Interface](#32-functionality--user-interface)

            -   [3.2.1 User system](#321-user-system)
            -   [3.2.3 Flashcard boxes](#323-flashcard-boxes)
            -   [3.2.4 Flashcards](#324-flashcards)
            -   [3.2.5 Statistics](#325-statistics)

        -   [3.3 Usability](#33-usability)

        -   [3.4 Reliability](#34-reliability)

            -   [3.4.1 Availability](#341-availability)
            -   [3.4.2 MTBF, MTTR](#342-mtbf-mttr)
            -   [3.4.3 Accuracy](#343-accuracy)
            -   [3.4.4 Bug classes](#344-bug-classes)

        -   [3.5 Performance](#35-performance)

            -   [3.5.1 Response time](#351-response-time)
            -   [3.5.2 Throughput](#352-throughput)
            -   [3.5.3 Capacity](#353-capacity)
            -   [3.5.4 Resource utilization](#354-resource-utilization)

        -   [3.6 Supportability](#36-supportability)

        -   [3.7 Design Constraints](#37-design-constraints)

            -   [3.7.1 Development tools](#371-development-tools)
            -   [3.7.2 Spring Boot](#372-spring-boot)
            -   [3.7.3 ReactJS](#373-reactjs)
            -   [3.7.4 Supported Platforms](#374-supported-platforms)

        -   [3.8 Online User Documentation and Help System Requirements](#38-online-user-documentation-and-help-system-requirements)

        -   [3.9 Purchased Components](#39-purchased-components)

        -   [3.10 Interfaces](#310-interfaces)

            -   [3.10.1 User Interfaces](#3101-user-interfaces)
            -   [3.10.2 Hardware Interfaces](#3102-hardware-interfaces)
            -   [3.10.3 Software Interfaces](#3103-software-interfaces)
            -   [3.10.4 Communications Interfaces](#3104-communications-interfaces)

        -   [3.11 Licensing Requirements](#311-licensing-requirements)

        -   [3.12 Legal, Copyright and other Notices](#312-legal-copyright-and-other-notices)

        -   [3.13 Applicable Standards](#313-applicable-standards)

    -   [4. Supporting Information](#4-supporting-information)

## 1. Introduction

### 1.1 Purpose
The project is an alternative to Discord and Teamspeak with self deployable servers,
it should prevent your data to be stored by other companys.

### 1.2 Scope
Ceangal Messenger should be able to have a text channel, which the user can create, as well as private messaging.
The servers should be deployable by the user and all data should be stored there.
Each user should be able to create a profile with which he can log in and customize his profile.
The users should also be able to add friends to their profile and be able to adjust their privacy.
These profiles should be also deployable.
Later on there should also be a voice channel.

### 1.3 Definitions, Acronyms and Abbreviations

| Term     |                                     |
| -------- | ----------------------------------- |
| **SRS**  | Software Requirements Specification |
| **JSON** | JavaScript Object Notation          |
| **API**  | Application Programming Interface   |
| **MTBF** | Mean Time Between Failures          |
| **MTTR** | Mean Time To Repair                 |
| **DTO**  | Data Transfer Object                |
| **HTTP** | Hypertext Transfer Protocol         |
| **FAQ**  | Frequently Asked Questions          |
| **REST** | Representational State Transfer     |
| **DNA**  | Do Not Applicable                   |
| **TBD**  | To Be Determined                    |

### 1.4 References

| Title                                                                                                 | Date       |
| ----------------------------------------------------------------------------------------------------- | ---------- |
| [Blog](https://ceangalmessenger.wordpress.com/)                                                       | 15/10/2020 |
| [GitHub --Code](https://github.com/LorenzSeufert/CeangalMessenger---Code)                             | 15/10/2020 |
| [GitHub --Documentation](https://github.com/LorenzSeufert/CeangalMessenger---Documentation)           | 15/10/2020 |
| [Use Case Diagram]()                                                                                  | 15/10/2020 |

### 1.5 Overview

## 2. Overall Description

### 2.1 Vision
Ceangal Messenger is a alternative to Discord and Teamspeak with self deployable servers. This is a Project for DHBW Karlsruhe from Lorenz Seufert, Lennart Royl, David Bullinger and Fabian Dittebrand.

## 2.2 Product perspective

### 2.3 User characteristics

### 2.4 Dependencies
- kotlin
- electron (?)

## 3. Specific Requirements

### 3.1 Functionality � Data Backend
- client based profiles (with a template)
- friends over servers
- chats
- channels

#### 3.1.1 Read data given over API endpoints
TBD

#### 3.1.2 Parse data
TBD

#### 3.1.3 Provide data
TBD

### 3.2 Functionality � User Interface
- Sign In
- Log In
- Create profile form after sign in
- Create server
- Join server (at least one but can also be many)
- Create channel
- Join channel

#### 3.2.1 User system
TBD

#### 3.2.3 Flashcard boxes
TBD

#### 3.2.4 Flashcards
TBD

#### 3.2.5 Statistics
TBD

### 3.3 Usability
TBD

### 3.4 Reliability
TBD

#### 3.4.1 Availability
- online

#### 3.4.2 MTBF, MTTR
TBD

#### 3.4.3 Accuracy
TBD

#### 3.4.4 Bug classes
TBD

### 3.5 Performance
TBD

#### 3.5.1 Response time
TBD

#### 3.5.2 Throughput
TBD

#### 3.5.3 Capacity
TBD

#### 3.5.4 Resource utilization
TBD

### 3.6 Supportability
TBD

### 3.7 Design Constraints
TBD

#### 3.7.1 Development tools
- Kotlin
- Electron (?)
- Mocha / JUnit
- YouTrack
- GitHub
- InteliJ
- MongoDB (?)

#### 3.7.2 Spring Boot
DNA

#### 3.7.3 ReactJS
DNA

#### 3.7.4 Supported Platforms
- PC

### 3.8 Online User Documentation and Help System Requirements
[GitHub](https://github.com/LorenzSeufert/CeangalMessenger---Documentation)

### 3.9 Purchased Components
TBD

### 3.10 Interfaces
TBD

#### 3.10.1 User Interfaces
TBD

#### 3.10.2 Hardware Interfaces
TBD

#### 3.10.3 Software Interfaces
TBD

#### 3.10.4 Communications Interfaces
TBD

### 3.11 Licensing Requirements
TBD

### 3.12 Legal, Copyright and other Notices
We do not take responsibilty for any incorrect data or errors in the application.

### 3.13 Applicable Standards
TBD

## 4. Supporting Information
For more information look into our [blog](https://ceangalmessenger.wordpress.com/)
