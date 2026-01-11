# Bug Reports

## Invalid booking payload returns 500 instead of 400

**Endpoint:** POST /booking

**Steps to reproduce:**
1. Send POST request to /booking
2. Use invalid payload (missing fields / wrong data types)

**Expected result:**
400 Bad Request

**Actual result:**
Sometimes returns 500 Internal Server Error

**Note:**
API validation appears unstable for invalid input.
