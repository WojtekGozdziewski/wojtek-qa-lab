# BUG-005: Inconsistent related record deletion behavior between CRM modules

## Summary
Deletion behavior between Contractors, Contacts and Sales Opportunities is inconsistent. The system does not always provide users with information about related records that may be affected by deletion.

## Module
- Contractors
- Contacts
- Sales Opportunities

## Environment
Defalto CRM

## Severity
High

## Priority
High

## Preconditions
User has access to CRM modules listed above.

## Steps to reproduce

### Scenario 1 - Delete Contractor linked to Sales Opportunity
1. Create a Contractor.
2. Create a Sales Opportunity linked to this Contractor through Organization.
3. Delete the Contractor.
4. Confirm deletion.

### Scenario 2 - Delete Contact linked to Sales Opportunity
1. Create a Contact.
2. Link the Contact with a Sales Opportunity.
3. Delete the Contact.
4. Confirm deletion.

### Scenario 3 - Delete Sales Opportunity linked to Contact and Contractor
1. Create a Sales Opportunity.
2. Link both Contact and Organization (Contractor).
3. Delete the Sales Opportunity.
4. Confirm deletion.

## Actual result
Observed behavior:
- Deleting a Contractor removes related Sales Opportunities.
- Deleting a Contact does not remove related Sales Opportunities.
- Deleting a Sales Opportunity removes the record without warning about existing Contact or Contractor relationships.

The system behavior is inconsistent depending on which related entity is deleted.

## Expected result
Deletion actions should have consistent dependency handling.

The system should:
- clearly inform the user about related records affected by deletion,
- prevent accidental loss of business data,
- apply consistent rules for relationships between Contractors, Contacts and Sales Opportunities.

## Business impact
Inconsistent deletion logic may lead to:
- unexpected loss of sales data,
- misunderstanding of CRM relationships,
- accidental deletion of records created or maintained by other users,
- reduced confidence in CRM data integrity.

## Notes
Further clarification of intended relationship rules between Contractors, Contacts and Sales Opportunities may be required.
