# Test Plan – Restful Booker API

## Objective
Verify core functionality, stability, and error handling of the Restful Booker REST API.

## Scope
In scope:
- Healthcheck endpoint
- Authentication and token handling
- Create booking (valid and invalid data)
- Get booking detail
- Negative scenarios (404 Not Found, invalid payloads)

Out of scope:
- Performance testing
- Security testing beyond basic auth
- UI testing

## Test Approach
- Manual API testing using Postman
- Automated execution using Newman (CLI)
- Assertions for:
  - HTTP status codes
  - Required response fields (contract testing)
  - Data correctness
- HTML report generated for automated runs

## Test Environment
- Public test API: https://restful-booker.herokuapp.com
- Tooling:
  - Postman
  - Newman + HTML reporter

## Test Data
- Static test data for booking creation
- Dynamic data handling using environment variables (token, bookingId)

## Entry Criteria
- API is accessible
- Postman collection and environment are configured

## Exit Criteria
- All critical tests executed
- No unexpected failures in Newman report
- Known API issues documented in BUG_REPORTS.md

## Risks and Notes
- Public API may be unstable
- Some invalid inputs may return 500 instead of 400 (documented as known issue)
