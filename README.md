# API Testing - DummyJSON (E-commerce Flow)

## Project Overview

This project demonstrates API testing skills using DummyJSON, simulating real-world QA scenarios for an e-commerce application.

The focus is on validating authentication, authorization, and product-related endpoints through functional, negative, and exploratory testing.

## Objectives
- Validate user authentication (login)
- Verify token-based authorization
- Test protected endpoints
- Validate product data and structure
- Identify potential security issues

## Scope
### In Scope
- Authentication (/auth/login)
- Authorized user data (/auth/me)
- Product edpoints (/products)

### Out of Scope
- UI testing
- Performance testing
- Database validation

## Tools Used
- Postman
- DummyJSON API
- VS Code

## Key Features Tested
### Authentication
- Valid login
- Invalid login
- Missing credentials
- Token-based access

### Security Testing
- Access without token ! (Bug Found)
- Access with invalid token

### Products
- Retrieve all products
- Retrieve product by ID
- Validate data structure
- Validate business logic (price, stock)

## Busgs Identified
### Critical Bug

- Protected endpoint `/auth/me` allows access without authentication
- Expected: 401 Unauthorized
- Actual: 200 OK

This represents a potential security vulnerability.

## Project Structure
```
api-testing-dummyjson/
├── README.md
├── test-plan.md
├── test-cases/
├── bug-reports/
├── postman-collection/
└── evidence/
    ├── auth/
    ├── inventory/
```

## How to Run the Tests
To execute these tests:

1. Download the JSON file from the `postman-collection` folder
2. Import it into your local Postman application
3. Run the requests and review the tests in the "Tests" tab

## Evidence
Screenshots with responses are available in the `evidence/` folder.

## Tester
Jorge Luis Garcia Zapata

Aspiring QA Engineer with hands-on experience in API, DevTools and manual testing, focused on building real-world testing scenarios and identifying critical issues.