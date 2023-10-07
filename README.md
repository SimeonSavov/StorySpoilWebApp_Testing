# StorySpoilWebApp_Testing
Welcome to the Story Spoil Web Application Testing repository. This repository contains all the information and documentation related to the manual testing of the Story Spoil web application based on the provided Software Requirements Specification (SRS) document.

## Overview

The primary objective of this testing effort is to ensure that the Story Spoil web application functions as expected according to the provided use cases outlined in the SRS document. This involves creating manual test cases for each use case and identifying and documenting any bugs or issues that are discovered during the testing process.

## Software Requirements

### Introduction

#### Purpose

The objective of this document is to provide a description of the Story Spoil application (also referred to as Story Spoil or The App). It will present an overview of the key functionalities.

#### Scope

This document includes high-level descriptions of the basic functionalities of Story Spoil, such as user registration, login, profile editing, spoiler creation, and management. It does not cover any special user (Administrator) functionalities.

### Overall Description

#### System Environment

The App hosts two primary actors: unregistered/non-logged users and registered/logged users. Both can access their respective parts of the application via the internet on the following URL:
[Story Spoil Web Application](https://d24hkho2ozf732.cloudfront.net/)

#### Key Features

- Unregistered/non-logged users have access only to the Home page of The App, with the option to either SIGN UP or LOG IN.
- Registered/logged users have access to main functionalities, including Profile editing, Spoiler creation, and Spoiler management.

### Use Cases

1. **Use Case 1 (Home Page)**: Users should be able to access The Story Spoil App from its designated URL via the Internet, which should load the Home page, appropriate to the user's logged-in status (unregistered/non-logged or registered/logged).

2. **Use Case 2 (User Registration)**: Unregistered users should be able to successfully go through the Sign-Up process. This involves the utilization of fields such as Username, Email, First name, Middle Name, Last name, Password, and Repeat Password, all subject to their respective constraints and character type acceptance.

3. **Use Case 3 (User Sign In)**: Registered users should be able to successfully go through the Log-In process. They should be able to log in using Username and Password.

4. **Use Case 4 (Profile Management)**: Upon successful Log-In, logged users should be able to navigate to their Profile page, edit their profile details, and view their Spoilers count. This involves the changing of profile picture inserted via URL, and editing of user data fields including First Name, Middle Name, Last Name, and About me sections.

5. **Use Case 5 (Spoiler Creation)**: Logged users should be able to navigate to the Create Spoiler page, where they can create a new Spoiler with a Title, Description, and a Picture (URL). After the Spoiler creation process, users should be redirected to the Home page, where the newly created Spoiler should be present.

6. **Use Case 6 (Spoiler Management)**: On the Home page, logged users should see all their Spoilers listed. Each Spoiler should have options for Share, Edit, and Delete. If no spoilers have been created yet, a "No Spoilers Yet!" message should be displayed. Users also should have the option to search for spoilers, based on spoiler titles.

## Testing Process

### Test Cases

All test cases created for the Story Spoil web application are documented in the 'Test Cases' directory of this repository. Each test case is designed to validate a specific functionality or use case described in the SRS document. -->
[TestCases](https://github.com/SimeonSavov/StorySpoilWebApp_Testing/tree/c894fc9395dfcdaae49b4973c1d7016dc242f999/TestCases)

### Bug Tracking

Any bugs or issues identified during the testing process are logged and tracked in the 'Bug Tracker' directory of this repository. Each bug report includes detailed information about the issue, steps to reproduce it. -->
[BugReports](https://github.com/SimeonSavov/StorySpoilWebApp_Testing/tree/c894fc9395dfcdaae49b4973c1d7016dc242f999/BugReports)

## API Testing with Postman

### Story Spoil API

This section provides information about the Story Spoil API endpoints and their functionalities. It serves as a guide to understand how to interact with the Story Spoil API.

**API Base URL:** [Story Spoil API](https://d5wfqm7y6yb3q.cloudfront.net/)

#### Supported Methods

You can see all the supported methods on the following link: [Methods](https://d5wfqm7y6yb3q.cloudfront.net/)

#### Endpoints

The following endpoints are supported:

1. **User**
   - `POST /api/User/Create` – Create a new user (post a JSON object in the request body).
   - `POST /api/User/Login` – Log in an existing user (post a JSON object in the request body).

   **Access Token:** When a user logs in, the response format is a JSON object containing an access token.

2. **Spoiler**
   - **All of the following requests require Authorization.**
   - `GET /api/Story/All` – List all spoilers.
   - `GET /api/Story/Search` – Search spoilers by their name (requires a query parameter: `?keyword=storyTitle`).
   - `POST /api/Story/Create` – Create a new spoiler (post a JSON object in the request body).
   - `PUT /api/Story/Edit/storyId` – Replace the existing spoiler with a new one (post a JSON object in the request body).
   - `DELETE /api/Story/Delete/storyId` – Delete an existing spoiler.

### Postman Requests

My task is to write API requests with Postman for certain RESTful API endpoints. I should organize the requests in a collection.

1. **Log in to the API**
   - Send a POST request with your username and password (previously created from the Story Spoil Web App).
   - If executed properly, you will receive your access token as part of the response body. Use it as a Bearer Token in the Authorization section for the next requests.

2. **Create a new spoiler**
   - Send a POST request with the attributes needed for creating a new spoiler.
   - The JSON body attributes include "title," "description," and an optional "url" for a picture.

3. **List all spoilers**
   - Send a GET request to receive a list of all created spoilers.

## Issues and Feedback

If you encounter any issues with the testing process or have feedback to improve it, please feel free to open an issue in this repository. Your feedback is valuable in ensuring the quality of the testing effort.

## Contact

For any questions or clarifications regarding the testing process, you can reach out to Simeon at simeonsavov21@gmail.com.


