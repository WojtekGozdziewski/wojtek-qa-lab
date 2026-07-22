# TC-001: Contractor duplicate validation

## Application

Defalto CRM (Cloud Trial)

## Module

Contractors

## Test objective

Verify that the system correctly handles creation of contractor records with identical names.

## Preconditions

- User is logged in.
- User has access to the Contractors module.

## Test data

Existing contractor:

Name: Kowalski  
NIP: 1111111111

New contractor:

Name: Kowalski  
NIP: 2222222222

## Test steps

1. Open the Contractors module.
2. Create a new contractor record.
3. Enter contractor data with the same name as an existing contractor.
4. Provide a different unique identifier (for example NIP).
5. Save the record.

## Expected result

The system should allow creation of a new contractor if the provided data represents a different business entity.

Duplicate detection should use appropriate unique identifiers and should not rely only on the contractor name.

## Actual result

The system prevents creation of a new contractor based only on the name field.

## Test result

Failed

## Related bug

BUG-001: Duplicate contractor validation based only on name field
