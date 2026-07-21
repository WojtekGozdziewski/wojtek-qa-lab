# BUG-001: Duplicate contractor validation based only on name field

## Application
Defalto CRM (Cloud Trial)

## Module
Contractors

## Severity
High

## Priority
High

## Summary

The system prevents creating multiple contractor records with the same name, treating the name field as a unique identifier.

This validation approach may prevent correct data management because different business entities can have identical names.

## Preconditions

- User has access to the Contractors module.
- Existing contractor record with a specific name is available.

## Steps to reproduce

1. Open the Contractors module.
2. Create a new contractor record.
3. Enter a contractor name, for example: "Kowalski".
4. Save the record.
5. Try to create another contractor with the same name but different business details.

## Actual result

The system prevents creating the second contractor record and reports it as a duplicate.

The validation is based only on the contractor name.

## Expected result

The system should allow creating different contractors with identical names.

Duplicate validation should use unique business identifiers, for example:
- Tax identification number (NIP)
- Internal contractor ID
- Other unique business identifier

## Business impact

Incorrect duplicate validation may lead to:

- inability to maintain accurate contractor records,
- incorrect contractor identification,
- inconsistent financial data,
- problems with reporting and accounting processes.

## Additional notes

A CRM system should maintain data integrity while allowing real-world cases where different entities have the same name.
