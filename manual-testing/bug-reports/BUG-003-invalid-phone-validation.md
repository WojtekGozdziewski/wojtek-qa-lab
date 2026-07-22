# BUG-003: Invalid phone number can be saved

## Module
Contractors

## Area
Create / Edit contractor form

## Field
Primary phone number

## Description
The system allows saving a contractor record with an invalid phone number.
The "Primary phone number" field is highlighted as invalid, but the validation does not prevent saving the record.

## Steps to reproduce
1. Open the Contractors module.
2. Create a new contractor or edit an existing contractor.
3. Enter an invalid phone number in the "Primary phone number" field, for example: `12`.
4. Click the Save button.

## Actual result
The "Primary phone number" field is highlighted as invalid, but the record is saved successfully.
The contractor is stored with an incorrect phone number.

## Expected result
The system should prevent saving the record until the phone number value is corrected.

Alternative behavior:
The system should display a warning message informing the user that the phone number is invalid and ask for confirmation before saving.

## Severity
Medium

## Priority
Medium

## Reproducibility
100%

## Business impact
Saving invalid phone numbers may reduce data quality in the CRM system and can lead to:
- inability to contact the contractor,
- incorrect communication attempts,
- unreliable contractor data.
