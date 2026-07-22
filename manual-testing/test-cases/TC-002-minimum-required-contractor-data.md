# TC-002: Verify minimum required data for creating a contractor

## Module
Contractors

## Objective
Verify the minimum set of data required to successfully create a new contractor record.

## Preconditions
- User is logged into the system.
- User has access to the Contractors module.

## Test steps
1. Open the Contractors module.
2. Click the button to create a new contractor.
3. Leave all optional fields empty.
4. Enter only the mandatory field(s).
5. Click the Save button.

## Test data
Contractor name:
`Test Contractor`

All other fields:
Empty

## Expected result
The system should enforce the minimum required information needed to create a contractor record.

Mandatory fields should provide enough information to uniquely identify the contractor and prevent creation of ambiguous records.

## Actual result
The system allows creating a contractor record with only the contractor name provided.

## Result
Pass / Fail

## Notes
If additional identifying information is required by business rules, the current validation allows creation of incomplete contractor records, which may lead to duplicate or ambiguous records in the database.
