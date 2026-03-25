# Authentication Test Cases

## TC-001: Valid Login
**Endpoint:** POST /auth/login

**Description:** Verify user can login with credentials

**Request Body:**
{
    "username": "emilys",
    "password": "emilyspass"
}

**Expected Result:**
- Status code 200
- Token is returned
- User data is returned

## TC-002: Invalid Login

**Endpoint:** POST /auth/login

**Description:** Verify login fails with incorrect credentials

**Request Body:**
{
    "username": "wrong",
    "password": "wrong"
}

**Expected Result:**
- Status code 400 or 401
- Error message returned

## TC-003: Missing Credentials

**Endpoint:** POST /auth/login

**Description:** Verify login fails when fields are missing

**Request Body:**
{
    "username": "emilys"
}

**Expected Result:**
- Status code 400
- Error message

## TC-004: Access Protected Endpoint with Token

**Endpoint:** GET /auth/me

**Description:** Verify access with valid token

**Expected Result:**
- Status code 200
- User data returned

## TC-005: Access whitout Token

**Endpoint:** GET /auth/me

**Description:** Verify access whitout token

**Expected Result:**
- Status code 401 (expected behavior)

## TC-006: Access with Invalid Token
**Endpoint:** GET /auth/me

**Description:** Verify access with invalid token

**Expected Result:**
- Status code 401