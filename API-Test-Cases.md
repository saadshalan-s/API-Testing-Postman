API Testing Test Cases
Project Overview
API testing performed using Postman to validate REST API endpoints, response status codes, response body, headers, and response time.
Test Cases
TC ID
Request
Method
Endpoint
Test Scenario
Expected Result
Actual Result
Status
API-TC-001
Get User by ID
GET
/users/1
Retrieve an existing user
Response status should be 200
200 OK
PASS
API-TC-002
Post Login Req
POST
/api/login
Login with valid credentials
Response status should be 200 and token should be returned
200 OK + Token
PASS
API-TC-003
Add User
POST
/users/add
Create a user with valid data
Response status should be 201
201 Created
PASS
API-TC-004
Add User - Invalid Age
POST
/users/add
Create a user with negative age
API should reject the invalid age
API returned 201 Created
FAIL
API-TC-005
Add User - Age Zero
POST
/users/add
Create a user with age = 0
Response status should be 201, valid JSON response, and response time below 1000 ms
All assertions passed
PASS
Tools
Postman
JavaScript Assertions
REST APIs
Defect
API-TC-004 identified that the API accepts a negative age and returns 201 Created instead of rejecting the invalid value.
The defect has already been documented in Jira.
