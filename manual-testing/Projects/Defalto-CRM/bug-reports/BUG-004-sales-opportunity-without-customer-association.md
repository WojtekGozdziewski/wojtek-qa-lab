# BUG-004: Sales Opportunity can be created without customer association

## Summary
The system allows users to create a Sales Opportunity without assigning any Contact or Organization (Contractor).

## Module
Sales Opportunities

## Environment
Defalto CRM

## Severity
High

## Priority
High

## Preconditions
User has access to the Sales Opportunities module.

## Steps to reproduce
1. Open the Sales Opportunities module.
2. Click "Add" to create a new Sales Opportunity.
3. Fill in only the required fields.
4. Leave Contact and Organization fields empty.
5. Save the record.

## Actual result
The Sales Opportunity is created successfully without any linked Contact or Organization.

## Expected result
The system should require at least one business relationship before saving:
- Contact, or
- Organization (Contractor)

Alternatively, the system should clearly inform the user that an unassigned Sales Opportunity is being created.

## Business impact
The system allows creation of sales records without identifying a customer or business entity.

This may lead to:
- orphaned sales opportunities,
- inaccurate sales pipeline data,
- difficulties identifying the responsible customer or contact,
- unreliable reporting.

## Notes
A Sales Opportunity represents a business process related to a customer relationship. Creating such records without any customer association may reduce data quality.
