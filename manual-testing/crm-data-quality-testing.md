# CRM Data Quality Testing

## Application
Defalto CRM (Cloud Trial)

## Test Area
Contractor management module

## Test Objective
Verify whether the system prevents incorrect contractor identification and maintains data quality during contractor creation.

## Test Scenario

### Scenario: Creating contractors with identical names

Steps:
1. Open Contractor module.
2. Create a new contractor.
3. Enter contractor name.
4. Save the record.
5. Attempt to create another contractor with the same name but different business details.

## Expected Result

The system should allow creation of different contractors if they represent different entities.

Duplicate validation should be based on unique business identifiers (for example tax identification number) rather than name only.

## Actual Result

The system prevents creating another contractor with the same name, treating the name field as a unique identifier.

The system does not provide a dedicated unique identifier that allows users to distinguish between contractors.

## Business Impact

Incorrect duplicate validation may lead to:
- inability to maintain accurate contractor records,
- duplicate or inconsistent data handling,
- incorrect contractor identification during daily operations,
- reduced reliability of financial and reporting processes.

## Severity

High

## Priority

High
