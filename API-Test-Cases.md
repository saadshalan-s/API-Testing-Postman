API Testing - Postman
Project Overview
This project demonstrates practical API testing using Postman.
The tests cover API requests, status codes, response body validation, headers, response time, positive testing, and negative testing.
Tools
Postman
JavaScript Assertions
REST APIs
API Test Cases
API-TC-001 — Get User by ID
Method: GET
Endpoint: https://dummyjson.com/users/1
Test Scenario: Retrieve an existing user.
Expected Result:
The API should return status code 200 OK.
Actual Result:
The API returned 200 OK.
Status: PASS
API-TC-002 — User Login
Method: POST
Endpoint: https://reqres.in/api/login
Test Scenario: Login using valid credentials.
Expected Result:
Status code should be 200 OK.
Response should contain a token.
Actual Result:
Status code: 200 OK.
Token was returned successfully.
Status: PASS
API-TC-003 — Add User
Method: POST
Endpoint: https://dummyjson.com/users/add
Test Scenario: Create a new user using valid data.
Expected Result:
The API should return status code 201 Created.
Actual Result:
The API returned 201 Created.
Status: PASS
API-TC-004 — Add User with Negative Age
Method: POST
Endpoint: https://dummyjson.com/users/add
Test Scenario: Create a user with a negative age.
Expected Result:
The API should reject the invalid age.
Actual Result:
The API accepted the negative age and returned 201 Created.
Status: FAIL
Defect:
The defect was documented in Jira.
API-TC-005 — Add User with Age Zero
Method: POST
Endpoint: https://dummyjson.com/users/add
Test Scenario: Create a user with age equal to zero.
Validations:
Status code should be 201.
Content-Type should be application/json.
Response time should be less than 1000 ms.
Age zero validation should pass according to the current API behavior.
Actual Result:
All four assertions passed successfully.
Status: PASS
Test Execution Summary
Total Requests: 5
Passed: 4
Failed: 1
Known Defect: 1
The failed test is a known validation defect related to accepting negative age values. The defect has already been documented in Jira.
Conclusion
The API collection was executed successfully using Postman.
The collection includes positive and negative test scenarios, response validation, status code assertions, response body validation, content-type validation, and response-time validation.
