# Bug Reports - Authentication

## BUG-001: Access to protected endpoint without autentication

**Endpoint:** GET /auth/me

**Severity:** Critical

**Priority:** High

### Description
The API allows access to a protected endpoint without providing an authentication token.

### Steps to Reproduce
1. Send a GET request to /auth/me
2. Do NOT include Authorization header

### Expected Result
- Status code 200 OK 
- User data is returned without authentication

### Impact
Unauthorized users can access sensitive user data without logging in, leading to potential security risks.

### Evidence
api-testing-dummyjson/ evidence/

## BUG-002: Inconsistent authentication validation

**Description**
The API rejects invalid tokens but allows requests with no token.

**Impact**
This inconsistency may lead to security loopholes.