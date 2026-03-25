# Products Test Cases

## TC-007: Get All Products

**Endpoint:** GET /products

**Description:** Verify all products are retrieved

**Expected Result:**
- Status code 200
- Response contains array of products

## TC-008: Get Product by Valid ID

**Endpoint:** GET /products/4

**Descrption:** Verify a product can be retrieved by ID

**Expected Result:**
- Status code 200
- Product data returned

## TC-009: Get Product by Invalid ID

**Endpoint:** GET /products/9999

**Description:** Verify behavior with non-existent product

**Expected Result:**
- Status code 404

## TC-010: Validate Products Data Structure

**Endpoint:** GET /products

**Description:** Verify product fields are present

**Expected Result:**
- Each product contains:
    - id
    - title
    - price
    - stock

## TC-011: Validate Product Data Logic

**Endpoint:** GET /products

**Description:** Verify product values are logical

**Expected Result:**
- Price > 0
- Stock >= 0
- No null critical fields