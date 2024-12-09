Here’s a **README.md** file that explains the provided API test suite using Playwright:

---

# API Test Suite with Playwright

This project demonstrates API testing using Playwright. It includes tests for HTTP methods such as DELETE, PUT, POST, and GET. Each test verifies the response status and validates response data.

## Prerequisites

- Node.js installed on your machine.
- Playwright installed globally or as a project dependency.

## Setup

1. Clone this repository or copy the code into your project directory.
2. Install Playwright and its dependencies:
   ```bash
   npm install @playwright/test
   ```

## Test Descriptions

### DELETE Request
- **Endpoint**: `https://reqres.in/api/users/2`
- **Purpose**: Deletes a user with ID `2`.
- **Expected Outcome**: The response status should be `204`.

### PUT Request
- **Endpoint**: `https://reqres.in/api/users/2`
- **Purpose**: Updates the user with ID `2`.
- **Payload**:
  ```json
  {
      "name": "Vithika",
      "job": "leader"
  }
  ```
- **Expected Outcome**: 
  - Response status should be `200`.
  - Response body should contain the name `Vithika`.

### POST Request
- **Endpoint**: `https://reqres.in/api/users/`
- **Purpose**: Creates a new user.
- **Payload**:
  ```json
  {
      "name": "Vithika",
      "job": "leader"
  }
  ```
- **Expected Outcome**:
  - Response status should be `201`.
  - Response body should contain the name `Vithika`.

### GET Request
- **Endpoint**: `https://reqres.in/api/users/2`
- **Purpose**: Retrieves details of a user with ID `2`.
- **Expected Outcome**:
  - Response status should be `200`.
  - Response body should contain the name `Janet`.

## Running the Tests

1. Run all tests using the Playwright Test Runner:
   ```bash
   npx playwright test
   ```

2. View detailed results:
   ```bash
   npx playwright test --reporter=list
   ```

## Notes

- Ensure you have internet connectivity since the tests interact with an external API (`https://reqres.in`).
- The tests log the JSON response to the console for easier debugging.

## Troubleshooting

- If tests fail due to response data mismatches, verify the API's availability and the endpoint's expected behavior.
- Use Playwright's debug mode to investigate failures:
   ```bash
   npx playwright test --debug
   ```

---
