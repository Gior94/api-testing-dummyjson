# Test Plan - DummyJSON API Testing

This project simulates real-world QA API testing scenarios.

## 1. Objective

The objective of this project is to validate the functionality, reliability, and security of the DummyJSON API, focusing on authentication and product-related endpoints.

## 2. Scope

### In Scope
- User authentication (login)
- Token-based authorization
- Access to protected endpoints
- Product retrieval and validation
- API response structure and status codes

### Out of Scope
- UI testing
- Performance testing
- Database validation

## 3. API Under Test

Base URL:
https://dummyjson.com

Endpoints:
- POST /auth/login
- GET /auth/me
- GET /products
- GET /products/{id}

## 4. Test Strategy

The testing approach includes:

- Functional testing
- Negative testing
- Security testing (basic authentication validation)
- Data validation
- Exploratory testing

## 5. Test Scenarios

### Authentication
- Valid login
- Invalid login
- Missing credentials
- Token usage
- Access whitout token
- Access with invalid token

### Products
- Retrieve all products
- Retrieve product by ID
- Invalid product ID
- Data consistency validation (price, stock, structure)

## 6. Test Environment

- Tool: Postman
- API: DummyJSON
- Format: JSON

## 7. Entry Criteria 

- API endpoints available
- Postman environment configured

## 8. Exit Criteria

- All planned test scenarios executed
- Bugs identified and documented
- API behavior analyzed

## 9. Risks

- API may not persist data (mock behavior)
- Some endpoints may not enforce strict validation
- Results may differ from real production systems

## 10. Deliverables

- Test Plan
- Test Cases
- Bug Reports
- Postman Collection
- Evidence (secreenshots)