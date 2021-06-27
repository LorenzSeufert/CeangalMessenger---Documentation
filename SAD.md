# Software Architecture Document

# Table of Contents

- [Introduction](#1-introduction)
    - [Purpose](#11-purpose)
    - [Scope](#12-scope)
    - [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [References](#14-references)
    - [Overview](#15-overview)
- [Architectural Representation](#2-architectural-representation)
- [Architectural Goals and Constraints](#3-architectural-goals-and-constraints)
- [Use-Case View](#4-use-case-view)
    - [Use-Case Realizations](#41-use-case-realizations)
- [Logical View](#5-logical-view)
    - [Overview](#51-overview)
- [Process View](#6-process-view)
- [Deployment View](#7-deployment-view)
- [Data View](#8-data-view)
- [Size and Performance](#9-size-and-performance)
- [Quality](#10-qualitymetrics)
- [Tools](#11-tools)

## 1. Introduction

### 1.1 Purpose

This document provides a comprehensive architectural overview of the system, using a number of different architectural
views to depict different aspects of the system. It is intended to capture and convey the significant architectural
decisions which have been made on the system.

### 1.2 Scope

The document describes the architecture of the Ceangal Messenger project. Including Use Cases, structure and
dependencies.

### 1.3 Definitions, Acronyms and Abbreviations

| Abbrevation | Description                            |
| ----------- | -------------------------------------- |
| REST        | Representational state transfer              |
| API         | Application programming interface                |
| MVC         | Model View Controller                  |
| n/a         | not applicable                         |

### 1.4 References

| Title                                                                                                                               |     Date     | Publishing organization   |
| ------------------------------------------------------------------------------------------------------------------------------------|:------------:| ------------------------- |
| [Ceangal-Messenger Blog](https://ceangalmessenger.wordpress.com/)                                                                            | 2020-12-03   | Ceangal-Messenger Team            |
| [Code Repository](https://github.com/LorenzSeufert/CeangalMessenger---Code)                                                          | 2020-12-03   | Ceangal-Messenger Team             |
| [Documentation Repository](https://github.com/LorenzSeufert/CeangalMessenger---Documentation)                                                      | 2020-12-03   | Ceangal-Messenger Team              |
| [Use Cases](https://github.com/LorenzSeufert/CeangalMessenger---Documentation/tree/main/UseCases)                                     | 2020-12-03  | Ceangal-Messenger Team  |
| [SRS](https://github.com/LorenzSeufert/CeangalMessenger---Documentation/blob/main/SRS.md)                                                      | 2020-12-03   | Ceangal-Messenger Team              |

### 1.5 Overview

The following contains the Architectural Representation, Goals and Constraints, the Use Case View and the Logical,
Process, Deployment, Implementation and Data views.

## 2. Architectural Representation

![Representation](Diagrams/MVC%20Diagram/ArchitecturalRepresentation.png)

## 3. Architectural Goals and Constraints

### Frontend

For the Frontend we are using the Electron Framework, which allows us to implement nice Desktop Applications with HTML,
CSS and JavaScript. And we use NodeJs and ExpressJs to make requests to our REST API

### Backend

In the Backend and Server we are using Kotlin with the Spring Framework. We use Spring Boot to create a REST API and
Spring Data JPA to communicate with the database.

### Database

For our database we are using MariaDB or an H2 Database in the development process.

### Patterns

We use a lot of patterns provided by our frameworks like Singleton, MVC, Proxy, etc. Also we use the builder pattern
provided by Kotlin through named arguments.

## 4. Use-Case View

![Use Case](UseCaseDiagram.png)

### 4.1 Use-Case Realizations

Each use case is documented by itself you can find it in
our [SRS](https://github.com/LorenzSeufert/CeangalMessenger---Documentation/blob/main/SRS.md)
or [here](https://github.com/LorenzSeufert/CeangalMessenger---Documentation/tree/main/UseCases)

## 5. Logical View

### Frontend

The different pages in the frontend are html/ejs files. These files get loaded and displayed by the Express server
running in parallel to the Electron Client. This makes it easy to load data in the Frontend from the Backend.

### Backend

The Backend is split into different API endpoints. There are some controller, services and model classes. The controller
are handling the incoming requests and outgoing responses. The services are processing the requests and access with the
models the database.

### 5.1 Overview

![MVC](Diagrams/MVC%20Diagram/MVC.png)

## 6. Process View

- When the user starts the frontend client, the Express server is starting, to display the pages. By using and clicking
  through the client the Express server renders the new pages and performs HTTP requests to the backend to get the
  required user data.

## 7. Deployment View

(n/a)

## 8. Data View

![ER-Diagram](Diagrams/Database%20Model/ER-Model-Ceangal-NEW.png)

## 9. Size and Performance

- The frontend is an Electron application, so it's not really lightweight but after the first start there are no real
  loading times.

- The backend can be run on every machine with Java so in the end it depends on the machine how long it takes to handle
  the requests.

## 10. Quality/Metrics

We use GitHub Actions for our CI pipeline. That means every push triggers the tests to make sure that all pushed code
works correctly. More about testing in
our [Testplan](https://github.com/LorenzSeufert/CeangalMessenger---Documentation/blob/main/TestPlan.md)

For code metrics we use Codacy. It gives us an overview what we can improve and do better in code style, etc. You can
find it [here](https://app.codacy.com/gh/LorenzSeufert/CeangalMessenger---Code/dashboard)

## 11. Tools

We use these tools for development:

- Version Control with git and [GitHub](https://github.com/LorenzSeufert/CeangalMessenger---Code)
- Project
  Management: [YouTrack](https://dhbw-karlsruhe.myjetbrains.com/youtrack/dashboard?id=8b4b5eb2-f674-4c03-8ea6-3c29a0a69b69)
- IDE: IntelliJ Ultimate
