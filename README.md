# DummyJSON API Testing

## Project Overview

This project demonstrates **API testing using Postman** on the DummyJSON REST API.

The project covers different HTTP methods including **GET, POST, PUT, PATCH, and DELETE**. Test cases were designed and executed to verify API functionality, response status codes, response data, input validation, and negative scenarios.

## Tools Used

- Postman
- REST API
- JavaScript
- Microsoft Excel
- GitHub

## API Methods Tested

### GET Requests

Tested scenarios include:

- Get all carts
- Get a single cart using a valid ID
- Get a single cart using an invalid ID
- Get carts for a valid user
- Get carts for an invalid user
- Get all products
- Get a single product using a valid ID
- Invalid resource scenarios

### POST Requests

Tested scenarios include:

- Login with valid credentials
- Login with invalid credentials
- Login with incorrect password
- Login with invalid username
- Add product with valid data
- Add product with multiple valid fields
- Add cart with valid data

### PUT / PATCH Requests

Tested scenarios include:

- Update cart product quantity
- Update product quantity to 1
- Update product quantity to 0
- Update product price
- Update product title
- Update with invalid Product ID
- Update with invalid Cart ID
- Update with negative quantity
- Update with decimal quantity
- Update with very large quantity

### DELETE Requests

Tested scenarios include:

- Delete product using a valid ID
- Delete product using an invalid ID
- Delete cart using a valid ID
- Delete cart using an invalid ID
- Delete cart using zero ID
- Delete product using zero ID

## Testing Types

The project includes:

- Functional Testing
- Positive Testing
- Negative Testing
- Boundary Value Testing
- Input Validation Testing
- Status Code Validation
- Response Body Validation
- API Response Verification

## Test Case Documentation

Detailed test cases and execution results are documented in the Excel file.

The test cases contain:

- Test Case ID
- Description
- Test Data
- Expected Result
- Actual Result
- Status

## Sample Test Results

| Test Case | Scenario | Status |
|---|---|---|
| GET TC-001 | Get all carts | Pass |
| GET TC-003 | Get cart with invalid ID | Pass |
| POST TC-001 | Login with valid credentials | Pass |
| POST TC-005 | Add product with valid title | Pass |
| PUT TC-001 | Update cart product quantity | Pass |
| PUT TC-006 | Update with invalid Product ID | Fail |
| DELETE TC-001 | Delete product using valid ID | Pass |
| DELETE TC-002 | Delete product using invalid ID | Pass |

## Validation Issues Identified

During testing, some negative and validation scenarios produced results different from the expected behavior defined in the test cases.

### Invalid Product ID

When updating a cart with an invalid Product ID, the API returned **HTTP 200 OK** instead of rejecting the invalid Product ID.

### Negative Quantity

The API accepted a negative product quantity and returned **HTTP 200 OK**.

### Decimal Quantity

The API accepted a decimal quantity such as **2.5** and returned **HTTP 200 OK** instead of rejecting the value.

These scenarios were documented as failed validation tests.

## Project Structure

```text
DummyJSON-API-Testing/
│
├── README.md
│
├── Test-Cases/
│   └── DummyJSON_API_Test_Cases.xlsx
│
├── Postman/
│   └── DummyJSON_API_Testing.postman_collection.json
│
└── Screenshots/
    ├── GET/
    ├── POST/
    ├── PUT-PATCH/
    └── DELETE/
```

## Key Learning

Through this project, I practiced:

- Creating API test cases
- Working with GET, POST, PUT, PATCH, and DELETE requests
- Creating Postman requests and collections
- Writing JavaScript test scripts in Postman
- Validating HTTP status codes
- Validating response body data
- Performing negative and boundary testing
- Identifying API validation issues
- Documenting actual and expected results
- Recording test execution status
